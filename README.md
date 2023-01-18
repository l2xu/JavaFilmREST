# JavaFilmREST
A small university project about a java gui with database connection.

## How to run this application
1. Create a database using a MariaDB compatible database management system (I used MySQL in XAMPP) named "prog3".
2. The database user is "root" and there is no password.
3. Import the "movies" table (the table.sql below) to the database.
4. Open the IntelliJ project.
5. Start the server.
6. Start the client.
7. When starting the client, the user can choose between the "normal" and "admin" user.



## tabelle.sql
SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
START TRANSACTION;
SET time_zone = "+00:00";

CREATE TABLE `movies` (
  `ID` int(11) NOT NULL,
  `Titel` varchar(300) NOT NULL,
  `Regisseure` varchar(300) NOT NULL,
  `Bewertung` tinyint(4) NOT NULL,
  `Genre` varchar(300) NOT NULL,
  `Laenge` smallint(6) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

INSERT INTO `movies` (`ID`, `Titel`, `Regisseure`, `Bewertung`, `Genre`, `Laenge`) VALUES
(39, 'Matrix Reloaded', 'Lana und Lilly Wachowski', 10, 'Action', 136),
(40, 'Rammstein: Paris', 'Jonas Åkerlund', 8, 'Musik', 98),
(41, 'Harry Potter und der Feuerkelch', 'Mike Newell', 6, 'Fantasy', 157);

ALTER TABLE `movies`
  ADD PRIMARY KEY (`ID`);
  
  ALTER TABLE `movies`
  MODIFY `ID` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=42;
COMMIT;
