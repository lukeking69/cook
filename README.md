# UFProdReg – UI-ændringer til NewWPF

[**Download UFProdReg-UI-Changes.zip**](https://raw.githubusercontent.com/lukeking69/cook/ufprodreg-ui-download/UFProdReg-UI-Changes.zip)

Pakken indeholder UI klar til senere binding: 21 separate Views og ViewModels, typed DTO-rækker, tomme valglister, navngivne ICommand-properties, fælles styles og statusindikatorer. Caliburn.Micro, MainMenu, SubMenu og ActiveItem følger den uploadede NewWPF-base. De nye sider indeholder ingen produktions-, database- eller hardwareimplementering.

Arkivet er en almindelig, ukrypteret ZIP på 128.892 bytes. Det indeholder kun 85 tilføjede og 9 ændrede filer, inklusive vejledning og filmanifest. Alle eksisterende NuGet-pakker og versionsnumre bevares.

1. Pak den oprindeligt uploadede `NewWPF_WithCaliburnMicro.zip` ud.
2. Pak ændringszippen ud med Windows' almindelige udpakker.
3. Kopiér zipindholdet til basens rodmappe, hvor `NewProgram.sln` ligger. Bevar undermapperne, og overskriv de eksisterende filer med samme navn.
4. Åbn løsningen i Visual Studio, gendan de originale NuGet-pakker fra virksomhedsfeeds, og vælg `newWPF` som startup-projekt med `Release | x86`.

Brug en frisk kopi af originalbasen til denne pakke. `README-UI-CHANGES.md` forklarer bindings og tilkobling af kommandoer. `UI-CHANGES.json` viser alle tilføjede/ændrede filstier med checksums.

XAML og kildekode kompilerer med 0 fejl og 0 advarsler mod .NET Framework 4.8. Cloudkontrollen brugte de reelle afhængighedsassemblies; lokale build-overrides og biblioteker er udeladt fra pakken. Layout og runtimebindings skal afprøves på Windows.

SHA-256: `78e1a36bfd80edb1402e6a1a41b1eaf7e63118d5d6b388578959dcb4c3b53a56`
