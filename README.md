# dock-releases

Runtime bundles for **thinknsh dock**, the container engine in ThinkNCollab Shell.
You don't need to download anything from here by hand:

```bash
npm install -g https://thinkncollab.com/downloads/dock/0.2.4/thinkncollab-shell.tgz
thinknsh dock setup
```

`thinknsh dock setup` picks the files for your OS and CPU and checks every file
against the sha256 in `manifest.json` before installing it.

## Layout

| Path | What it is |
| --- | --- |
| `manifest.json` | Manifest of the latest version |
| `<version>/manifest.json` | `{ version, files: { name: { sha256, size } } }` |
| `<version>/tnc-dock-vm-{aarch64,x86_64}.tar.gz` | macOS Linux VM (Apple Silicon / Intel) |
| `<version>/tnc-vz-darwin-universal` | macOS VM launcher (both CPUs) |
| `<version>/tnc-dock-wsl-{x86_64,aarch64}.tar.gz` | Windows WSL2 distro (x64 / ARM64) |
| `<version>/tnc-shim-linux-*`, `crun-linux-*` | Native Linux runtime |
| `<version>/thinkncollab-shell.tgz` | thinknsh itself |

Downloads and the guide: https://thinkncollab.com/dock
