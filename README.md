# Test App - license detection nuget

- trivy parses \*.nuspec files found inside `$NUGET_PACKAGES` folder or `$HOME/.nuget/packages/` to fetch license information of a given packages

## Filesystem

1. Clone the repo
2. Easy way to use dotnet is to install `nix` (https://nixos.org/download#download-nix)
3. Run `nix-shell -p dotnet-sdk_8 dotnetPackages.Nuget` inside the cloned folder.
4. Run `dotnet restore`. This will populate the .nuspec files in corresponding folder ($HOME/.nuget/packages)
5. Run filesystem scan

- To install additional packages use `dotnet add package <package-name>` (https://www.nuget.org/packages)

## Image

1. Run `docker build -t <image-name> .`
2. Scan the image
