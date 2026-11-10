# Fritchii_OoT_Windows11_Script_By_Naxacid
Made this for my friend... Think anyone with windows 11 can benefit from it. Easy to stay update and not do everything step by step, even if everything is easy, it takes time... I hate waste time! enjoy :)

# Fritchii OoT Windows 11 setup package

## English

### What is included

- `Fritchii_OoT_Extreme_Cache_60FPS_Windows11.cmd` installs or updates the latest official Windows x64 Fritchii build, configures the Windows gaming settings in the script, and creates desktop shortcuts for Fritchii and Ocarina of Time.
- This guide explains how to prepare the game file.
- `Fritchii_Windows11_Script_Overview.docx` describes the complete behavior of the setup script.

The package does **not** include Ocarina of Time, game keys, firmware, or other copyrighted game data. The user must provide a game copy they are legally entitled to use. Obtain and prepare it from your own game and console using a method permitted by your local law and Fritchii's documentation. The setup script cannot download the game for you.

### Install and run

1. Extract this package into a folder where you want Fritchii installed. Keep the CMD file in that folder.
2. Create a subfolder named `Spel` next to the CMD file.
3. Place your own Fritchii-compatible Ocarina of Time game container (`.nup`) in `Spel`. The setup automatically detects a matching `.nup` file. If there are several matching versions, it selects the highest version it can identify.
4. Run the CMD file. It requests administrator approval so it can create and activate the persistent Windows power plan. It checks current Fritchii news and the local installation, downloads the latest official Windows x64 emulator build when needed, and creates desktop shortcuts.
5. If the game file is stored elsewhere, launch from PowerShell with `& "C:\path\Fritchii_OoT_Extreme_Cache_60FPS_Windows11.cmd" -GameFile "C:\path\your-game.nup"`.

To preview setup actions without applying them, run `& ".\Fritchii_OoT_Extreme_Cache_60FPS_Windows11.cmd" -DryRun` from PowerShell.

### Permanent performance power plan

The script creates a persistent `Fritchii Maximum Performance` Windows plan from the built-in High Performance plan when available, or from Balanced on systems that do not expose High Performance. It activates aggressive processor boost and 100% minimum and maximum processor states for AC power and battery, and selects active cooling. The plan remains active after Fritchii closes. Windows firmware, thermal limits, and device policy can still restrict actual CPU boost. This setting applies to Windows generally, not only while the emulator runs.

To restore the power plan that was active before setup and remove the script-managed plan, run the CMD file with `-Revert`. Revert also requests administrator approval.

Shader and pipeline caches are preserved so Fritchii can reuse them across game restarts and new playthroughs. The script does not erase game saves. Let Fritchii finish its own shader preparation after an update or driver change.

## Svenska

### Det här ingår

- `Fritchii_OoT_Extreme_Cache_60FPS_Windows11.cmd` installerar eller uppdaterar den senaste officiella Windows x64-versionen av Fritchii, ställer in skriptets Windows-spelinställningar och skapar skrivbordsikoner för Fritchii och Ocarina of Time.
- Den här guiden visar hur du placerar spelfilen.
- `Fritchii_Windows11_Script_Overview.docx` beskriver alla funktioner i installationsskriptet.

Paketet innehåller **inte** Ocarina of Time, spelnycklar, firmware eller annat upphovsrättsskyddat spelinnehåll. Användaren måste själv tillhandahålla en spelkopia som hen har laglig rätt att använda. Skaffa och förbered den från ditt eget spel och din egen konsol med en metod som är tillåten enligt lokal lag och Fritchiis dokumentation. Skriptet kan inte hämta spelet åt dig.

### Installera och starta

1. Packa upp paketet i mappen där du vill ha Fritchii. Låt CMD-filen ligga kvar där.
2. Skapa en undermapp som heter `Spel` bredvid CMD-filen.
3. Lägg din egen Fritchii-kompatibla Ocarina of Time-spelfil (`.nup`) i `Spel`. Installationen hittar en matchande `.nup` automatiskt. Om flera versioner hittas väljs den högsta version som skriptet kan identifiera.
4. Kör CMD-filen. Den ber om administratörsgodkännande så att den kan skapa och aktivera den permanenta Windows-prestandaplanen. Den kontrollerar aktuella Fritchii-nyheter och installationen, hämtar den senaste officiella Windows x64-versionen när det behövs och skapar skrivbordsikoner.
5. Om spelfilen ligger någon annanstans kan du starta via PowerShell med `& "C:\sökväg\Fritchii_OoT_Extreme_Cache_60FPS_Windows11.cmd" -GameFile "C:\sökväg\ditt-spel.nup"`.

För att förhandsgranska åtgärder utan att verkställa dem, kör `& ".\Fritchii_OoT_Extreme_Cache_60FPS_Windows11.cmd" -DryRun` i PowerShell.

### Permanent prestandaplan

Skriptet skapar en permanent Windows-plan som heter `Fritchii Maximum Performance`. Den utgår från High Performance när det finns, annars från Balanced. Den ställer processorboost på Aggressive, minsta och högsta processorläge på 100 % för både nätström och batteri samt aktiv kylning. Planen förblir aktiv när Fritchii stängs. Firmware, temperaturgränser och datorns policy kan fortfarande begränsa faktisk CPU-boost. Inställningen gäller Windows generellt, inte bara när emulatorn körs.

Kör CMD-filen med `-Revert` för att återställa planen som var aktiv före installationen och ta bort Fritchiis plan. Även återställningen ber om administratörsgodkännande.

Shader- och pipeline-cachar bevaras så att Fritchii kan återanvända dem efter omstart och vid en ny spelomgång. Skriptet raderar inte sparfiler. Låt Fritchii slutföra sin shaderförberedelse efter uppdatering eller drivrutinsbyte.
