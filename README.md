# KRPG Language Support

<div align="center">

**English** | [Русский](README.ru.md)

</div>

Visual Studio Code extension providing syntax highlighting and language support for KRPG (Kotazzz RPG) - a domain-specific language for creating text-based RPG games.

## Features

- **Syntax Highlighting**: Full syntax highlighting for KRPG language constructs
- **Comment Support**: Line comments with `#`
- **Bracket Matching**: Auto-completion and matching for `{}`, `[]`, `()`
- **String Support**: Double-quoted strings with escape sequences
- **Keyword Recognition**: Highlights KRPG-specific keywords and commands

### Supported Language Elements

#### Sections
- `init` - Game initialization
- `scenarios` - Story scenarios
- `items` - Item definitions
- `npcs` - Non-player character definitions
- `locations` - Game world locations
- `quests` - Quest definitions

#### Control Flow
- `if`, `while`, `for` - Conditional and loop constructs
- `return`, `goto`, `stop`, `wait` - Flow control
- `require`, `multiple`, `option` - Special flow controls

#### Declarations
- `action`, `stage` - Action and stage definitions
- `item`, `npc`, `location` - Entity declarations
- `link`, `lock`, `unlock` - Location management
- `start`, `end`, `goal` - Quest mechanics
- `complete`, `evolve`, `quest` - Game state changes

#### Variables and Constants
- Variables starting with `_` (e.g., `_random`, `_time`)
- UPPERCASE constants (e.g., `WEAPON`, `ARMOR`)
- Numbers and quoted strings

## Example

```krpg
# Game initialization
init {
    say "Welcome to the adventure!"
    quest main_story
}

# Define items
items {
    sword "Iron Sword" "A sturdy iron blade" {
        slot_type WEAPON
    }
}

# Define NPCs
npcs {
    guard "Village Guard" "A friendly guard" {
        stage {
            action talk "Talk to guard" {
                say guard "Hello, traveler!"
                say you "Good day!"
            }
        }
    }
}

# Define locations
locations {
    village "Village Square" "The heart of the village" {
        npc guard
        item sword
    }
    
    start village
}
```

## About KRPG

KRPG is a domain-specific language created by [kotazzz](https://github.com/kotazzz) for building text-based RPG games. The language provides a declarative syntax for defining game worlds, characters, items, quests, and interactive storylines.

### Key Features of KRPG Games:
- Rich storytelling with branching narratives
- Complex character interactions
- Item and inventory management
- Quest systems with multiple objectives
- Location-based exploration
- Combat and skill systems

## Related Projects

- [KRPG Game Engine](https://github.com/kotazzz/krpg) - The main KRPG game engine
- [Discord Community](https://discord.gg/FKcURWZsMW) - Join the KRPG community
- [Telegram Channel](https://t.me/krpgd) - Latest updates and discussions

## Installation

1. Install the extension from the VS Code marketplace
2. Open any `.krpg` file to see syntax highlighting in action
3. Start creating your own text-based RPG adventures!

## Contributing

If you find issues or want to contribute to the language support:

1. Report bugs on the [GitHub Issues](https://github.com/kotazzz/krpg/issues) page
2. Join the community on [Discord](https://discord.gg/FKcURWZsMW) or [Telegram](https://t.me/krpgd)
3. Check out the main [KRPG project](https://github.com/kotazzz/krpg) for more information

## License

This extension is released under the MIT License. See the main KRPG project for more details.

---

**Enjoy creating amazing text-based RPG adventures with KRPG!**
