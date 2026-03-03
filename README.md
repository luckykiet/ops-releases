# OPS Peripherals — Releases

Pre-built Windows installers for **OPS Peripherals**.

## Downloads

Go to the [Releases](../../releases) page and download the latest installer for your architecture:

| File | Architecture |
|------|-------------|
| `ops-peripherals-<version>-x64-setup.exe` | 64-bit (recommended) |
| `ops-peripherals-<version>-ia32-setup.exe` | 32-bit |

## System Requirements

- Windows 10 or later
- Node.js 20–24 (bundled with Electron, no separate install needed)

## Auto-Update

The application checks for updates automatically. When a new release is published here, running instances will prompt to download and install.

## Publishing

Maintainers: use `yarn release` from the source repository to build and upload new installers.

A `scripts/config.env` file is required (copy from `scripts/config.example.env`):

```env
GITEA_URL=https://gitea.com
GITEA_TOKEN=<your-gitea-token>
GITHUB_TOKEN=<your-github-token>
OWNER=<owner>
REPO=ops-releases
```

## Generating API Tokens

### GitHub

1. Go to **Settings → Developer settings → Personal access tokens → Fine-grained tokens**
   https://github.com/settings/personal-access-tokens/new
2. Set a name and expiration
3. **Repository access** → select `ops-releases`
4. **Permissions → Repository permissions** → **Contents**: Read and write
5. Click **Generate token** and copy it immediately

### Gitea

1. Go to **Settings → Applications → Manage Access Tokens**
   `https://<your-gitea-url>/user/settings/applications`
2. Enter a token name
3. **Select permissions** → **repository**: Read and write
4. Click **Generate Token** and copy it immediately
