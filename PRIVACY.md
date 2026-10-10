# Privacy Policy for LingoHUD

**Effective date:** applies to LingoHUD 1.2 and later (date set at release)
**Publisher:** Scrapline Studio

LingoHUD is a Windows desktop application. It has no account system, no servers of ours, no telemetry and no analytics. This page explains exactly what stays on your computer and what can leave it.

## 1. What stays on your computer

- **Screen text recognition (OCR).** Screenshots are processed locally. LingoHUD never uploads a screenshot.
- **Speech recognition.** System audio and microphone audio are transcribed locally with the bundled Whisper models, or with a local speech model you add yourself.
- **Local translation.** The Hy-MT2, MADLAD-400 and M2M-100 engines run on your computer. If you add your own GGUF model, or connect LM Studio or Ollama running on your own computer, that traffic stays on your machine (127.0.0.1).
- **Translation history.** LingoHUD keeps a local history in `%APPDATA%\LingoHUD\history.db`: recognized text, its translation, the language pair, the active profile and the title of the window that was in front. It is kept until you clear it, unless you choose a 30/90/365-day limit in *Settings → Privacy and local data*. You can search it, export it to CSV, or clear it from the tray menu.
- **Settings and logs.** Settings and log files live in `%APPDATA%\LingoHUD\`. Logs mask user text at normal log levels.
- **Diagnostics.** The tray's *Debug Export* and the optional audio/capture diagnostics write files only to your computer, after showing you what they contain. They leave your computer only if you choose to share them.

## 2. What can leave your computer, and only when you choose it

| Feature | What is sent | Sent to |
|---|---|---|
| Read-aloud and "speak it" output, with the online voice (the default voice; used only when you ask for speech) | The text LingoHUD speaks | Microsoft Edge online voice service |
| Optional model downloads (only when you click **Download** in the model catalog) | A normal download request. No screen content, audio or translated text is sent. | Hugging Face (or the source shown in the app) |

All translation in LingoHUD runs on your computer. Switching to Windows system voices keeps speech fully on your computer as well.

The Steam version of LingoHUD does **not** offer cloud speech recognition or cloud AI providers that use your own API key.

## 3. Sensitive text

Before screen text is translated, LingoHUD masks recognized passwords, API keys, tokens and similar credentials where it can detect them. Masked lines are not sent to any translation engine. Detection is pattern-based and cannot catch everything, so avoid translating screens that show secrets.

## 4. Voice typing and publisher captions

- **Voice typing** only listens while you hold the push-to-talk key, press its hotkey or click the microphone button. Its result goes to the clipboard, is typed into the active window (only with your consent; LingoHUD never presses Enter), or is spoken into a virtual microphone, as you choose.
- **Publisher captions** show your speech in a local window and a local text file for streaming software such as OBS. Nothing is uploaded by LingoHUD. What your streaming software broadcasts is up to you.

Both features are off by default.

## 5. Children

LingoHUD is not directed at children and does not knowingly collect any personal data from anyone.

## 6. Changes

If this policy changes, the new version will be published here with a new effective date and mentioned in the Steam update notes.

## 7. Contact

Questions about privacy: open an issue in this repository, post in the LingoHUD Steam discussions, or contact us on Discord.
