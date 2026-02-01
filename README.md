## Troubleshooting

### macOS: "App is damaged and can't be opened"

If you download the app from GitHub Releases and see a message saying **"Plot.app is damaged and can't be opened"**, this is because the app is not code-signed with an Apple Developer Certificate. macOS Gatekeeper blocks unsigned apps downloaded from the internet.

**Solution:**
Run the following command in your terminal to remove the quarantine verification for the app:

```bash
xattr -cr /path/to/Plot.app
```

Or if you installed it to `/Applications`:

```bash
xattr -cr /Applications/Plot.app
```
