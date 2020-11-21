# ptest

CREATE TABLE salas (
  id_sala INT(11) NOT NULL,
  nombre VARCHAR(45) NOT NULL,
  id_pelicula INT(11),
  PRIMARY KEY (id_sala));

CREATE TABLE peliculas (
  id_pelicula INT(11) NOT NULL,
  nombre VARCHAR(45) NOT NULL,
  edad_minima INT(11),
  PRIMARY KEY (id_pelicula));

ALTER TABLE salas ADD CONSTRAINT fk_salas_peliculas
  FOREIGN KEY (id_pelicula)
  REFERENCES peliculas (id_pelicula);


INSERT INTO peliculas (id_pelicula, nombre, edad_minima)
VALUES (1, 'Pelicula 1', 0);
INSERT INTO peliculas (id_pelicula, nombre, edad_minima)
VALUES (2, 'Pelicula 2', 7);
INSERT INTO peliculas (id_pelicula, nombre, edad_minima)
VALUES (3, 'Pelicula 3', 12);
INSERT INTO peliculas (id_pelicula, nombre, edad_minima)
VALUES (4, 'Pelicula 4', 12);
INSERT INTO peliculas (id_pelicula, nombre, edad_minima)
VALUES (5, 'Pelicula 5', 16);
INSERT INTO peliculas (id_pelicula, nombre, edad_minima)
VALUES (6, 'Pelicula 6', null);

INSERT INTO salas (id_sala, nombre, id_pelicula)
VALUES (1, 'Sala 1a', 1);
INSERT INTO salas (id_sala, nombre, id_pelicula)
VALUES (2, 'Sala 2a', null);
INSERT INTO salas (id_sala, nombre, id_pelicula)
VALUES (3, 'Sala 11a', 1);
INSERT INTO salas (id_sala, nombre, id_pelicula)
VALUES (4, 'Sala 12a', 4);
INSERT INTO salas (id_sala, nombre, id_pelicula)
VALUES (5, 'Sala 1b', 5);
INSERT INTO salas (id_sala, nombre, id_pelicula)
VALUES (6, 'Sala 2b', 6);
