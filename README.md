# Pacman
<b><h3>Aplicación de Escritorio Java - Demo Juego Pacman</h3></b>
Juego desarrollado para Plataforma Java y mediante API Java Standar Edition.
La misma se desarrolló implementado una arquitectura MVC para una mayor independencia entre sus componentes y/o paquetes de clases, facilidad en el mantenimiento en caso de errores y posibilitando el escalamiento de la aplicación en caso de ser requerido.<br>
Además la misma cuenta con conexión a base de datos mediante MySQL y la utilización de procedimientos almacenados, aunque esto último no es necesario ya que no habrá sobrecarga resultante de comunicar grandes cantidades de datos salientes y entrantes por tratarse de una aplicación de escritorio con fines lúdicos. <br>
A continuación, se detalla en simples pasos la configuración de la BBDD requerida para un mejor uso de la aplicación. <br>
<b><h3>BASE DE DATOS</h3></b>
<b><p>1) Creación de la BBDD en servidor MySQL denominándola <i>pacman</i></p></b>
<b><p>2) Creación de la tabla:</p></b>
create table score (<br>
nombre varchar(20),<br>
palabra varchar(20),<br>
puntos int,<br>
fecha varchar(20)<br>
)<br>
<b><p>2) Creación de los procedimientos almacenados:</p></b>
CREATE PROCEDURE INSERTAR_PACMAN (<br>
nom VARCHAR(20),<br>
punt INT(20),<br>
intent INT(11),<br>
fech DATE )<br>
BEGIN<br>
INSERT INTO score (nombre, puntos, fecha)<br>
VALUES(nom , punt , fec);<br>
END<br><br>
CREATE PROCEDURE CONSULTAR_PACMAN ()<br>
BEGIN<br>
SELECT * FROM score ORDER BY puntos DESC LIMIT 3;;<br>
END<br><br>
