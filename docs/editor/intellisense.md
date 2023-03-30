# Intellisense

Intellisense is a powerful code completion tool that suggests symbols and code snippets for you as you type. It is available in the Monaco Editor by default.

## Configuration

You can configure the behavior of Intellisense in the Monaco Editor by providing an `IEditorOptions` object with the desired settings. Here are some of the options you can configure:

### Suggest Selection

The `suggestSelection` option controls the history mode for suggestions. It can be one of the following values:

- `'first'`: Always select the first suggestion.
- `'last'`: Select the last used suggestion.
- `'recentlyUsed'`: Select the most recently used suggestion.
- `'recentlyUsedByPrefix'`: Select the most recently used suggestion that starts with the same prefix as the current word.

```typescript
monaco.editor.create(document.getElementById('container'), {
    value: 'console.log("Hello, world!");',
    language: 'javascript',
    suggestSelection: 'recentlyUsedByPrefix'
});
```

### Suggest Font Size

The `suggestFontSize` option controls the font size for the suggest widget. It defaults to the editor font size.

```typescript
monaco.editor.create(document.getElementById('container'), {
    value: 'console.log("Hello, world!");',
    language: 'javascript',
    suggestFontSize: 16
});
```

### Suggest Line Height

The `suggestLineHeight` option controls the line height for the suggest widget. It defaults to the editor line height.

```typescript
monaco.editor.create(document.getElementById('container'), {
    value: 'console.log("Hello, world!");',
    language: 'javascript',
    suggestLineHeight: 20
});
```

### Suggest on Trigger Characters

The `suggestOnTriggerCharacters` option controls whether suggestions should automatically show when typing trigger characters. It defaults to `true`.

```typescript
monaco.editor.create(document.getElementById('container'), {
    value: 'console.log("Hello, world!");',
    language: 'javascript',
    suggestOnTriggerCharacters: false
});
```

### Tab Completion

The `tabCompletion` option controls the behavior of the Tab key when suggestions are visible. It can be one of the following values:

- `'on'`: Insert the best matching suggestion when the Tab key is pressed.
- `'off'`: Do not insert suggestions on Tab key press.
- `'onlySnippets'`: Insert the best matching snippet on Tab key press.

```typescript
monaco.editor.create(document.getElementById('container'), {
    value: 'console.log("Hello, world!");',
    language: 'javascript',
    tabCompletion: 'on'
});
```

### Tab Index

The `tabIndex` option controls the tab index of the editor's textarea.

```typescript
monaco.editor.create(document.getElementById('container'), {
    value: 'console.log("Hello, world!");',
    language: 'javascript',
    tabIndex: 1
});
```

### Unicode Highlighting

The `unicodeHighlighting` option controls the Unicode highlighting settings.

```typescript
monaco.editor.create(document.getElementById('container'), {
    value: 'console.log("Hello, world!");',
    language: 'javascript',
    unicodeHighlighting: {
        // Your custom settings
    }
});
```

For more information on configuring the Monaco Editor, refer to the [official documentation](https://microsoft.github.io/monaco-editor/api/interfaces/monaco.editor.ieditoroptions.html).