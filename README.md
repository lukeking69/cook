# UFProdReg – bindbar UI og kontrolrettelse

[**Download rettelseszippen til dit eksisterende UI-projekt**](https://raw.githubusercontent.com/lukeking69/cook/ufprodreg-ui-download/UFProdReg-UI-Control-Fix.zip) – 8.164 bytes.

Rettelsen medtager komplette XAML/code-behind-par for StatusBadgeView, StepProgressView og StepLabelView samt deres enum og projektfil. Kontrollerne registreres eksplicit som Page/Compile uden dubletter. Text/State-bindings og workspace-funktionalitet bevares.

1. Luk Visual Studio, og kopiér zipindholdet til projektets rodmappe, hvor NewProgram.sln ligger. Medtag både projektfilen og .xaml.cs-filerne.
2. Hvis projektfilen har egne tilpasninger, sammenflet kun den kommenterede kontrolgruppe fra den leverede newWPF.csproj. Bevar egne referencer og øvrige tilpasninger.
3. Fjern de genererede newWPF/bin- og newWPF/obj-mapper, åbn løsningen, og kør Rebuild med Release | x86.

README-CONTROL-FIX.md forklarer installationen; UI-CONTROL-FIX.json angiver checksums. Rettelseszippen ændrer fem kildefiler og medtager tre uændrede kontrolafhængigheder for komplette filpar.

MC3072 om Text kan reproduceres ved at udelade StatusBadgeView.xaml.cs fra kompileringen. MC3074 på MainView.xaml linje 104 kan reproduceres ved at udelade StepProgressView-filparret. Den faktiske lokale udeladelsesårsag er ikke påvist; den nye pakke gør kontrolfilernes inkludering eksplicit.

## Komplet ændringspakke til en frisk base

[**Download UFProdReg-UI-Changes-v2.zip**](https://raw.githubusercontent.com/lukeking69/cook/ufprodreg-ui-download/UFProdReg-UI-Changes-v2.zip) – 130.927 bytes.

Pakken indeholder alle UI-ændringer mod den oprindeligt uploadede NewWPF-base, inklusive kontrolrettelsen: 85 tilføjede og 12 ændrede filer. Der er 21 separate Views/ViewModels, typed DTO-rækker, tomme valglister, ICommand-properties, fælles styles og statusindikatorer. Caliburn.Micro, MainMenu, SubMenu og ActiveItem følger basen. Ingen produktions-, database- eller hardwareimplementation er tilføjet.

Pak originalbasen ud, og kopiér hele ændringszipindholdet til mappen med NewProgram.sln. Alle eksisterende NuGet-pakker og versionsnumre er bevaret; virksomhedens originale feeds kræves til restore. Læs README-UI-CHANGES.md og UI-CHANGES.json i pakken.

## Kontrol

Begge arkiver er almindelige, ukrypterede Deflate-ZIP. Rettelsen er bygget fra en ren kildekopi med 0 fejl og 0 advarsler mod .NET Framework 4.8 med basens reelle afhængigheder. Lokale build-overrides og biblioteker er udeladt fra leverancerne. Windows-layout og runtimebindings skal stadig afprøves på Windows.

SHA-256 rettelseszip: `a52b16c5f367c82c0a7129b4784d16fde0fadf514a9e5cab3e1385aa2631d115`

SHA-256 komplet v2: `5a44631891c1c0bb0e5f87b90e7399cc04d0785e750215b26e6cadd2579137ad`
