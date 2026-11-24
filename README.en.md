# Naskvoz · Насквозь

A Windows app that tests and selects local DPI bypass configurations for YouTube, Discord and other sites. It checks HTTPS endpoints and YouTube video servers separately.

[Русская инструкция](README.md) · [Download for Windows x64](https://github.com/RedTowerInc/naskvoz/releases/latest/download/Naskvoz-Windows-x64.zip) · [Telegram: @AndyMooren](https://t.me/AndyMooren)

![Naskvoz main window with the active profile and YouTube and Discord checks](docs/screenshots/main.png)

## Run

1. Download `Naskvoz-Windows-x64.zip` from [Releases](https://github.com/RedTowerInc/naskvoz/releases/latest).
2. Extract the entire `Naskvoz` folder. Keep `_internal`, `engines` and `config` next to the executable.
3. Run `Naskvoz.exe` as administrator and press the central button. The first run selects and verifies a configuration for your connection.

Requires Windows 10/11 x64. The archive includes the graphics engine, Python and required libraries. The app works locally on your PC.

The current release is **2.0.3**. The download is about **203 MiB**, or **482 MiB** extracted. Startup has been tested on Windows 10 Pro 22H2 x64.

Auto-selection can combine different profiles for websites and video servers. The app tests the combination together and saves it as soon as selection finishes. The next time you turn it on, the app runs a short check of the saved configuration.

If a CDN times out but each service still has a confirmed endpoint, the app saves the configuration with a warning. If selection finds no workable configuration, use **«Подобрать заново»** (try again) to start a new search. Stop any other DPI bypass engine before running the app.

The main card shows the selected configuration. **«Составная схема»** means several profiles are used for different sites or video servers. Press **«Состав схемы»** to view their names and domains; they are also listed on the Profiles page. Use **«Проверить схему»** to check the saved result, or **«Профили → Подобрать новую схему»** to request a new selection. Full comparison remains available in Settings; the first confirmed configuration may not be the fastest in the catalog.

To update, close the app and extract the new archive into a separate folder. Copy **`data`** from the previous `Naskvoz` folder to preserve settings and the last working configuration. A fresh folder needs an initial selection.

If the window flickers, open **«Параметры → Отрисовка окна»** (Settings → Rendering), select **«Совместимая (статичная)»** (Compatibility), save and restart. This mode uses a static background.

HTTPS checks do not verify Discord voice. Passing the selected YouTube CDN checks does not guarantee uninterrupted playback for every video or network route. The app reports failed checks instead of treating a running engine as proof of service availability.

The app keeps settings and reports in `data` next to the executable. It does not change system DNS, proxy settings, firewall rules or startup entries. Closing the app stops its own engine.

## Contact

Report bugs through [Issues](https://github.com/RedTowerInc/naskvoz/issues) or contact [AndyMooren on Telegram](https://t.me/AndyMooren).

This repository contains the ready-to-run Windows release, instructions and screenshots. Third-party notices are included in the distribution.

The application source project is not published here. GitHub's automatic **Source code** archives contain only documentation and images. Download **Naskvoz-Windows-x64.zip** from Releases to run the app.
