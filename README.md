# link-over-copy-paste

An attempt to turn copy and pasting into linking.

When you copy in an app `⌘+C`, and paste `⌘+V` into another you duplicate content and the receiving end cannot lead you to the original context.

I propose a different mechanism: When you copy, a long-lived process will capture the context, including the app, file open, selection, and sub-app location. This context is then injected into the clipboard, alongside the copied content. What this means is that compatible applications can now link to the original context instead of just copying, by reading the link in the clipboard. And non-compatible applications still have access to the copied content.

The context is injected into the clipboard in the form of a [x-callback-url](http://x-callback-url.com/) style link. Applications that allow to fully re-evoke context through their own x-callback-url link schemes will have those injected in the clipboard. For the rest, this project will provide its own x-callback-url scheme as a fallback (example: `link-to-context://x-callback-url/context?app=MyEditor&file=draft.txt&selection=1234,1240`).
