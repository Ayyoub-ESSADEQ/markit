# Markit
**Markit** is a minimal markdown editor that gets synced with local files. You just need to import your markdown file, and any changes made will be automatically saved to the local file.

![](https://github.com/Ayyoub-ESSADEQ/markit/blob/main/screenshots/markdown-editor.png?raw=true)

# Why?
I have tested many other open-source projects for online markdown editors, but unfortunately, all of them only support uploading and persisting changes to cloud storage like Google Drive, Dropbox, and so on.

I'm a huge fan of the local-first approach, so I committed to building this app. It didn't take long, but I hope it will provide the necessary functionality to mimic normal markdown editors.

# How It Works
The idea behind Markit is that you can import or create markdown files and be able to make changes persist on your local system with an auto-save option.

I achieved these functionalities by combining two things: a markdown editor and the File System Access API.

- **Markdown editor**: To implement markdown editor features, I relied on [Lexical](https://github.com/facebook/lexical), a rich text editor recently created by Facebook. When the user wants to import a markdown file, I read the file content and use `$convertFromMarkdownString` to convert the markdown text file to an `editorState` so that Lexical can render it properly.

- **File System Access API**: This is a web API that allows access to users' local files so that they can import, create, and persist changes to the imported files.

## Credits
- [Lexical](https://github.com/facebook/lexical): A modern text editor developed by Facebook, designed for flexibility and extensibility.
- [Text Editor](https://github.com/GoogleChromeLabs/text-editor/): A demo created by Peter LePage showcasing the capabilities of the File System Access API.