# mclauncher
The old launcher we all know and love with the quality-of-life features of the new launcher. This aims to support java 8 through modern java.

## How to use
1. Go to the [latest release](https://github.com/RagedMeteor1837/mclauncher/releases/latest)
2. Download the `mclauncher-xxx-redist.jar` file
3. Run it

## Features
- Microsoft authentication
- Bundled JVMs
  - Automatically downloads the appropriate JVM for all minecraft versions
  - You just need a runtime to open the actual launcher
  - You can still provide your own JVMs
- Update checking

## Planned Features
- Add skin/cape management

## How to build from source
The commands must be run in the following order to build from source:
- `decompile.sh`
  - Downloads original jar and decompiles it
- `init.sh`
  - Turns decompiled sources into a git repository
- `applyPatches.sh`
  - Applies OLauncher patches to the decompiled sources
- `mvn clean package`
  - Compiles the patched launcher
- `genredist.sh` (optional)
  - Make sure you've run `git submodule update --init` as this script uses the `AutoOL` submodule.
  - Generates the redistributable JAR - Do not distribute the JARs in `olauncher/target`!
