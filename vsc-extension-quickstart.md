# KRPG Language Support Extension

## What's in the folder

* This folder contains all files for the KRPG Language Support extension
* `package.json` - Extension manifest declaring KRPG language support and grammar location
* `syntaxes/krpg.tmLanguage.json` - TextMate grammar file for KRPG tokenization
* `language-configuration.json` - Language configuration for comments, brackets, and auto-completion

## Get up and running

* Press `F5` to open a new Extension Development Host window with your extension loaded
* Create a new file with `.krpg` extension
* Verify that syntax highlighting works for KRPG constructs:
  - Sections: `init`, `scenarios`, `items`, `npcs`, `locations`, `quests`
  - Keywords: `if`, `while`, `action`, `stage`, etc.
  - Comments: Lines starting with `#`
  - Strings: Double-quoted text
  - Variables: Words starting with `_`
  - Constants: UPPERCASE words

## Test your extension

Create a test file `test.krpg` with this content:

```krpg
# This is a comment
init {
    say "Hello, KRPG world!"
    quest test_quest
}

items {
    sword "Test Sword" "A test weapon" {
        slot_type WEAPON
    }
}

npcs {
    guard "Test Guard" "A test NPC" {
        stage {
            action talk "Talk" {
                say guard "Hello!"
                if "_condition" {
                    say "Conditional text"
                }
            }
        }
    }
}
```

## Make changes

* You can relaunch the extension from the debug toolbar after changing files
* You can also reload (`Ctrl+R` or `Cmd+R` on Mac) the Extension Development Host window
* Changes to `syntaxes/krpg.tmLanguage.json` require reloading the window
* Changes to `language-configuration.json` take effect immediately

## Add more language features

To enhance KRPG language support:

* **IntelliSense**: Add completion providers for KRPG keywords and constructs
* **Hover Information**: Provide documentation on hover for KRPG elements
* **Error Detection**: Validate KRPG syntax and show diagnostics
* **Code Snippets**: Add common KRPG patterns as snippets
* **Folding**: Enable code folding for sections and blocks

Check the [VS Code Language Extensions Guide](https://code.visualstudio.com/api/language-extensions/overview) for implementation details.

## Install your extension

* To use locally: Copy to `<user home>/.vscode/extensions` folder and restart VS Code
* To publish: Use `vsce publish` after setting up your publisher account
* See [Publishing Extensions](https://code.visualstudio.com/api/working-with-extensions/publishing-extension) for details

## About KRPG

KRPG is a domain-specific language for creating text-based RPG games, developed by [kotazzz](https://github.com/kotazzz). 

* [Main KRPG Project](https://github.com/kotazzz/krpg)
* [Discord Community](https://discord.gg/FKcURWZsMW)
* [Telegram Channel](https://t.me/krpgd)
