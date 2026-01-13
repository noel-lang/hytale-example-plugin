# HelloPlugin

A simple example plugin for Hytale servers demonstrating the basics of plugin development.

## Features

- Registers a `/hello` command
- Displays a title message to players when executed

## Requirements

- Java 17+
- Hytale Server API (`HytaleServer.jar`)

## Getting HytaleServer.jar

You need the `HytaleServer.jar` file to compile plugins. There are two ways to obtain it:

### Option 1: From Hytale Launcher

After installing the Hytale Launcher, you can find the server files in:

| OS      | Path                                                            |
|---------|-----------------------------------------------------------------|
| Windows | `%appdata%\Hytale\install\release\package\game\latest`          |
| Linux   | `$XDG_DATA_HOME/Hytale/install/release/package/game/latest`     |
| macOS   | `~/Application Support/Hytale/install/release/package/game/latest` |

Copy `HytaleServer.jar` from that directory into the `libs/` folder of this project.

### Option 2: Hytale Downloader CLI

For production servers, you can use the official **Hytale Downloader CLI** tool to download the latest server files. This requires OAuth2 authentication.

For more details, see the official [Hytale Server Manual](https://support.hytale.com/hc/en-us/articles/45326769420827-Hytale-Server-Manual).

## Building

1. Place `HytaleServer.jar` in the `libs/` directory
2. Build with Gradle:

```bash
./gradlew build
```

The compiled plugin JAR will be located at `build/libs/HelloPlugin-1.0-SNAPSHOT.jar`.

## Installation

Copy the built JAR file to your Hytale server's `plugins/` directory.

## Usage

In-game, use the command:

```
/hello
```

This will display a title message saying "Hello world!" to the player.

## Project Structure

```
src/main/java/com/example/plugin/
├── HelloPlugin.java    # Main plugin class
└── HelloCommand.java   # Command implementation
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
