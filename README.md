# Tabhush

Hit Start from wherever you are. Tabhush figures out what you're working on, quiets every unrelated app and site until you're done, and shows you where your time went. A desktop app for macOS and Windows; everything is decided and stored on your computer.

This repo holds the installers for Mac and Windows and the update feed installed Windows copies check. The app's source is private.

## Download

<a href="https://github.com/ajeetb123/tabhush-releases/releases/latest"><img alt="Download Tabhush" src="https://img.shields.io/github/v/release/ajeetb123/tabhush-releases?label=Download&logo=github&style=for-the-badge&color=2ea44f"></a>

**[Get the latest version](https://github.com/ajeetb123/tabhush-releases/releases/latest)** and pick the file for your computer:

```
Mac with Apple Silicon (M1 and newer)   Tabhush-<version>-arm64.dmg
Mac with Intel                          Tabhush-<version>-x64.dmg
Windows 10 / 11                         Tabhush-Setup-<version>.exe
```

Not sure which Mac you have? Apple menu → About This Mac. "Chip: Apple M…" means arm64, "Processor: Intel" means x64. macOS 13 or newer.

### Install on Mac

1. Open the `.dmg` and drag **Tabhush** into **Applications**.
2. Open Tabhush from Applications. Tabhush isn't signed with an Apple Developer ID yet, so macOS says it can't verify it. Click **Done**.
3. Go to **System Settings → Privacy & Security**, scroll down to "Tabhush was blocked", and click **Open Anyway**. You only do this once.
4. When Tabhush asks for **Accessibility** and to control your browser (**Automation**), allow both. It uses them to read window and tab titles and close distracting tabs. Nothing leaves your Mac.

If step 3 doesn't show the button, run this once in Terminal and open the app again:

```bash
xattr -dr com.apple.quarantine /Applications/Tabhush.app
```

Mac copies don't update themselves yet. To upgrade, download the new `.dmg` and replace the app in Applications; your sessions and settings stay.

### Install on Windows

1. Run `Tabhush-Setup-<version>.exe`. It installs for your account only (no admin) and opens Tabhush.
2. If Windows says "Windows protected your PC", click **More info → Run anyway**. The installer isn't code-signed yet.

Windows copies update themselves in the background and never restart during a session.

### Good to know

- During a locked session, Tabhush can't be quit, and force-quitting relaunches it. End the session first.
- Your data stays on your computer: `~/Library/Application Support/Tabhush` on Mac, `%APPDATA%\Tabhush` on Windows.
