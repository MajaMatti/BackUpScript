@Echo off
echo.
MODE 100,40
COLOR 09
set jahr=%date:~-4%
set monat=%date:~-7,2%
set tag=%date:~-10,2%
set stunde=%time:~0,2%
set minute=%time:~3,2%
echo.
echo   Datum/Uhrzeit: %tag%.%monat%.%jahr% %stunde%:%minute%
echo   Autor:         MHO
echo   Erstellt:      26/07/2020
echo.
echo   ==========================================================================
echo   Backup mit Windows Robocopy 
echo   ==========================================================================
echo.
echo   Kopierart: Es werden nur Dateien Kopiert die im Zielverzeichnis nicht bereits vorhanden sind. 
echo              Ausgenommen sind Dateien mit 
echo              neuerer Version im Quellenverzeichnis.
echo.              
echo.
echo   Optionen:  /MIR  Komplette Spiegelung des Quellverzeichnisses,
echo                    in der Quelle nicht mehr vorhandene Dateien werden
echo                    im Ziel ebenfalls geloescht
echo              /V    Erweiterte Informationen nach dem Kopieren anzeigen
echo              /NP   Fortschrittsanzeige waehrend des Kopierens ausblenden
echo              /XO   Dateien, die im Zielordner als "neuer" gekennzeichnet
echo                    sind, werden NICHT ueberschrieben
echo              /DST  Probleme nach Sommer/Winterzeitumstellung vermeiden
echo                    (ab Robocopy-Version XP026)
echo              /R:10 Anzahl der Wiederholversuche nach Kopierfehler
echo              /W:30 Wartezeit zwischen den Wiederholversuchen in Sekunden
echo.
echo   Wahlweise: /XF  Exkludierte Dateien (Wildcards moeglich)
echo              /XD  Exkludierte Ordner (Wildcards moeglich)
echo              /L   Simuliert den Kopiervorgang, es wird nichts kopiert
echo                   oder geloescht (VOR DEM ERSTEN EINSATZ EMPFOHLEN!)
echo.
echo                   Alle Optionen erhalten Sie mit ROBOCOPY /?
echo.
echo   ==========================================================================
echo.
echo   Aktuelle Spezifikation:
echo.
echo   **************************************************************************************
echo   ROBOCOPY "C:\Users\Matti\Desktop\Source" "C:\Users\Matti\Desktop\Target" 
echo             /V /XO /DST /R:10 /W:30 /ETA /LOG:C:\Users\Matti\Desktop\Source\log.txt /TEE
echo   **************************************************************************************
echo.
:Eingabeaufforderung
echo   	Soll der Kopiervorgang gestartet werden?
echo.
echo    	[1] Fortfahren
echo		[2] Abbrechen
echo.
set /P Eingabe=
if /i "%Eingabe%"=="1" goto CopyStart
if /i "%Eingabe%"=="2" goto eof
echo Falsche Eingabe - Bitte nur 1 oder 2 eingeben
goto :Eingabeaufforderung
echo.
pause
echo.


:CopyStart
echo.
@Echo off
::chcp 1252
echo.
ROBOCOPY "C:\Users\Matti\Desktop\Source" "C:\Users\Matti\Desktop\Target" /V /XO /DST /R:10 /W:30 /ETA /LOG:C:\Users\Matti\Desktop\Source\log.txt /TEE

echo.
@Echo off
::chcp 850
echo.
@Echo off
echo.
echo.
echo   Der Kopiervorgang wurde abgeschlossen!

echo.
pause
