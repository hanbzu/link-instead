# ~~copy and paste~~ link instead!

Turning copy and paste into linking.

When you copy `⌘+C` and paste `⌘+V` you loose the ability to bring you back to the source. Content is simply duplicated. **What if you could turn these quick copy-and-paste operations into deep linking operations?**

I propose an extension: When you copy, a long-lived process will capture the context, including app, open file, selection, and sub-app location. This context is then injected into the clipboard, alongside the copied content. What this means is that compatible applications can now link to the original context instead of just copying, by reading the link in the clipboard. Non-compatible applications still have access to the copied content.

The potential for this is a new inter-application operation layer in the form of links. You would be able to open your text editor and create a list of tasks that refer to data in different applications, for example. Or refer to a quote that opens in your favourite ebook reader.

The context is injected into the clipboard in the form of a [x-callback-url](http://x-callback-url.com/) style link. Applications that allow to fully re-evoke context through their own x-callback-url link schemes will have those injected in the clipboard. For the rest, this project will provide its own x-callback-url scheme as a fallback (example: `link-to-context://x-callback-url/context?app=MyEditor&file=draft.txt&selection=1234,1240`).

## I need help 🆘

Ideally, this would be an extension compatible with the main desktop OSs: Linux, MacOS and Windows. Which means the program needs to interact with OS Clipboard and/or Accessibility APIs.

I just don't have the experience and attention span to develop this on my own.

**If you have some clues on how to build this and would like to join me in creating this as an Open Source tool, please [tell me](mailto:hibai.unzueta@hey.com).**

## Work in progress
