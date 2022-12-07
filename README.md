# Die Idee:
	Dieses Script kann benutzt werden um Backups zu vereinfachen. Hierzu werden von einem wahlweise zentralem 
	Speicherverzeichnis aus symbolische Links auf das System verteilt. Wodurch sich die Verzeichnisstruktur die
	in einem Backup beruecksichtigt werden soll ueberschaubarer gehalten werden kann. Etwaigige Broken Links,
	die durch Aenderungen im Quellverzeichnis entstehen werden regelmaessig geloescht.

# Einrichtung:
	lnk2.conf: 
		-> erwarteter Ablageort :  ~/.config/lnk2/lnk2.conf
		-> Hier koennen die Quell- und Zielverzeichnisse deklariert werden

	lnk2:
		-> moeglicher Ablageort : /usr/local/bin/lnk2
		-> hierbei handelt es sich um die Binary
		-> zunaechst wuerden alle "Broken links" geloescht werden, dies ist per default auskommentiert
		-> lnk2.conf wird unter dem erwarteten Ablageort gesourct
		-> wenn das Element aus dem Quellverz. am Ziel nicht existiert wird es dort symbolisch verlinkt

# Automatisierung:
	-> ein regelmaessiges Aufrufen des Scriptes kann zum Beispiel durch crontab erfolgen
	-> commandline Befehl fuer einen minuetlichen Aufruf ist:
	
	$ crontab -e

	and enter:
	* * * * * /Pfad/zur/binary
