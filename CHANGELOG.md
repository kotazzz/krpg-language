# Change Log

All notable changes to the "KRPG Language Support" extension will be documented in this file.

Check [Keep a Changelog](http://keepachangelog.com/) for recommendations on how to structure this file.

## [1.0.0] - 2025-06-30

### Added
- Initial release of KRPG Language Support extension
- Complete syntax highlighting for KRPG language constructs
- Support for all KRPG sections: `init`, `scenarios`, `items`, `npcs`, `locations`, `quests`
- Keyword highlighting for control flow: `if`, `while`, `for`, `return`, `goto`, `stop`, `wait`, `require`, `multiple`, `option`
- Declaration keyword support: `action`, `stage`, `item`, `npc`, `location`, `link`, `lock`, `unlock`, `start`, `end`, `goal`, `complete`, `evolve`, `quest`
- Variable highlighting for underscore-prefixed variables (e.g., `_random`, `_time`)
- Constant highlighting for UPPERCASE identifiers
- String literal support with escape sequences
- Comment support using `#` character
- Bracket matching and auto-completion for `{}`, `[]`, `()`
- Number literal recognition
- Command highlighting for line-starting identifiers

### Language Features
- Full TextMate grammar definition for KRPG
- Proper scoping for syntax highlighting themes
- Auto-closing pairs for brackets and quotes
- Surrounding pairs for text selection
- Line comment configuration

## [Unreleased]

### Planned Features
- IntelliSense support for KRPG keywords
- Code snippets for common KRPG constructs
- Error detection and validation
- Hover information for KRPG elements
- Go to definition support
- Code folding for sections and blocks