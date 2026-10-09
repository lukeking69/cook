# UFProdReg – UI og bindingsrettelser

[**Download rettelsen til OperatorName-fejlen**](https://raw.githubusercontent.com/lukeking69/cook/ufprodreg-ui-download/UFProdReg-UI-Binding-Fix.zip) – 3.681 bytes.

Pakken ændrer kun MainView.xaml fra det senest uploadede projekt. De tre Run.Text-bindings til OperatorName, LoginRemainingSeconds og TechnicianName bruger nu Mode=OneWay. Run.Text bruger ellers som standard TwoWay, hvilket fejler for disse skrivebeskyttede properties. ViewModels og loginlogik er uændret.

1. Luk programmet og Visual Studio.
2. Pak zippen ud, og kopiér newWPF/Views/MainView.xaml til den tilsvarende placering i projektet.
3. Åbn løsningen, rebuild og start programmet.

Den uploadede fils øvrige bytes, inklusive layouttilpasninger og linjeskift, er bevaret. README-BINDING-FIX.md forklarer rettelsen; UI-BINDING-FIX.json angiver checksums.

## Komplet ændringspakke til en frisk base

[**Download UFProdReg-UI-Changes-v3.zip**](https://raw.githubusercontent.com/lukeking69/cook/ufprodreg-ui-download/UFProdReg-UI-Changes-v3.zip) – 131.117 bytes.

Pakken indeholder alle UI-ændringer mod den oprindeligt uploadede NewWPF-base, inklusive kontrol- og bindingsrettelser: 85 tilføjede og 12 ændrede filer. Der er 21 separate Views/ViewModels, typed DTO-rækker, tomme valglister, ICommand-properties, fælles styles og statusindikatorer. Caliburn.Micro, MainMenu, SubMenu og ActiveItem følger basen. Ingen produktions-, database- eller hardwareimplementation er tilføjet.

Pak originalbasen ud, og kopiér hele ændringszipindholdet til mappen med NewProgram.sln. Eksisterende NuGet-pakker og versionsnumre er bevaret; virksomhedens originale feeds kræves til restore. Læs README-UI-CHANGES.md og UI-CHANGES.json i pakken. Brug den lille bindingszip til det allerede tilpassede projekt; v3-pakken bruger det generelle layout fra UI-leveringen.

## Tidligere kontrolrettelse

[Download UFProdReg-UI-Control-Fix.zip](https://raw.githubusercontent.com/lukeking69/cook/ufprodreg-ui-download/UFProdReg-UI-Control-Fix.zip).

Denne pakke medtager komplette XAML/code-behind-par og eksplicit Page/Compile-registrering til de tidligere MC3072/MC3074-fejl. Den er allerede inkluderet i v3. Ved egne projektfiltilpasninger sammenflettes den kommenterede kontrolgruppe; vejledningen findes i arkivet.

## Kontrol

Alle arkiver er almindelige, ukrypterede Deflate-ZIP. Det korrigerede uploadede projekt og den generelle v3-kode kompilerer hver med 0 fejl og 0 advarsler mod .NET Framework 4.8 med basens reelle afhængigheder. Lokale build-overrides og biblioteker er udeladt. Bindings til skrivebeskyttede properties er gennemgået; WPF-runtime er ikke afprøvet på Windows i cloudkontrollen.

SHA-256 bindingszip: `2f39608deb9dd7859653ab455f1adfad054a87ad395984aea7b15e030d483410`

SHA-256 komplet v3: `7506f3e78f47af48f5a2acd5e925f5901aae72dc91d801fba0416e4ce2a3d4fc`
