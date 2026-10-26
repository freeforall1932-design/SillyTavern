# SillyTavern for Windows

A Windows-only, runtime-focused distribution of SillyTavern, an LLM frontend for power users.

## Requirements

- **Windows 10 or Windows 11**
- **Node.js 20 or newer** — download the current LTS installer from <https://nodejs.org/>
- An internet connection for the first launch, so npm can download the required production packages

> Extract the archive to a folder you can write to, such as `C:\SillyTavern`. Do **not** use `C:\Program Files`, OneDrive-synchronised folders, or an archive viewer.

## Install and run

1. Download the Windows archive and extract it completely.
2. Double-click **`Start.bat`**.
3. On its first run, it installs only the production dependencies and creates your local `data` folder.
4. Leave the command window running and open <http://127.0.0.1:8000> in your browser.

Your chats, characters, settings, and other private data are stored in `data`. Back up that folder before moving or replacing the installation.

## Updating

### Git installation

If this folder was cloned with Git, double-click **`UpdateAndStart.bat`**. It downloads updates and starts the app. Git is required only for this update method.

### Downloaded archive

1. Download and extract the newer Windows archive to a **new** folder.
2. Copy the `data` folder from the old installation into the new one.
3. Start the new copy with `Start.bat`.
4. Confirm your content is available before deleting the old folder.

Do not copy the entire `public` folder from an old installation; it contains application files, not just your data.

## Optional features retained

- **Docker Desktop on Windows:** `docker compose -f docker/docker-compose.yml up -d --build`
- **Electron wrapper:** run `Start.bat` inside `src\electron` after installing the main application.
- **Remote access:** `Remote-Link.cmd` creates a temporary Cloudflare tunnel. Only use it if you understand the security implications and have configured authentication in `config.yaml`.

## What was removed

This distribution removes non-Windows launch scripts, hosted-notebook and Replit files, repository automation, contributor/security policy files, and fork-maintenance tooling. The core server, interface, model tokenizers, default content, Windows launchers, production dependency lockfile, Docker integration, and Electron Windows launcher remain intact.

## Resources

- Documentation: <https://docs.sillytavern.app/>
- Upstream project: <https://github.com/SillyTavern/SillyTavern>
- License: [AGPL-3.0](LICENSE)
