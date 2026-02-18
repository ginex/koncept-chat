Koncept Chat Site

This static site introduces Koncept Chat and hosts an update manifest for the app.

Structure
- index.html: Landing page with a download button and version display.
- manifest.json: Update metadata consumed by Koncept Agent.
- styles.css: Simple styling.
- assets/: Place 'koncept-logo.png' here for the header.
- .nojekyll: Disables Jekyll processing on GitHub Pages.

Manifest schema
```
{
  "version": "1.0.1",
  "downloadUrl": "https://github.com/<owner>/<repo>/releases/download/v1.0.1/Koncept-Chat-Setup-1.0.1.exe",
  "notes": "Optional release notes"
}
```

Publish to GitHub Pages
1. Create a new public repository (e.g., 'koncept-chat').
2. Copy this folder's contents into the repo root.
3. Commit and push.
4. In GitHub: Settings → Pages → Build and deployment → Deploy from a branch.
   - Source: 'main'; Folder: '/(root)'. Save.
5. After deployment, your site will be at: `https://<user>.github.io/koncept-chat/`.
   - The manifest will be at: `https://<user>.github.io/koncept-chat/manifest.json`.

Configure Koncept Agent
- Set `updateManifestUrl` in `Koncept-Agent/config/config.json` to your manifest URL above.
- The app will show an update button only when the remote version differs from the installed version.
