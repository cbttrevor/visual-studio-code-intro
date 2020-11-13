## Learning Objectives

One of the customizable features in Visual Studio Code are keyboard shortcuts, also known as key bindings.

### Open the Key Binding Editor

To access the custom key bindings, hit `F1` to invoke the Command Palette and search for `key jso`.
This search should yield the full command name: `Preferences: Open Keyboard Shortcuts (JSON)`.

### Add a Custom Key Binding

To add a custom key binding to your VSCode configuration, add a new JSON object under the root array.
As you start typing, you'll notice that the editor helps valdiate the correctness of your JSON object.
Once you create a new JSON object, you'll probably see a message saying `Missing property "key"`.
That indicates that you need to add a new property named `key` to the JSON object, in order for it to be a valid key binding.

#### Required Properties

The only properties that you're required to add to a new key binding are `key` and `command`.
One common pitfall of key bindings is putting spaces between the characters.
Instead of `SHIFT + ALT + X` use `SHIFT+ALT+X` to ensure that your key binding works properly.

```
// Place your key bindings in this file to override the defaults
[
    {
        "key": "SHIFT+ALT+X",
        "command":"saveAll"
    }
]
```

### Troubleshooting Keyboard Shortcuts

In some cases, you might encounter a problem with a keyboard shortcut that doesn't work, or exhibits unexpected behavior.
If this happens, you can invoke the keyboard shortcuts troubleshooter.

Press `F1` and search for `key tro`, which should locate the full command `Developer: Toggle Keyboard Shortcuts Troubleshooting`.

If you see a message in the log saying `No keybinding entries`, then your key binding's `key` property should be more closely examined.