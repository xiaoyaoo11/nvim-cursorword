## Cursorword

A concise, precise, and high-performance cursor word highlighting plugin for Neovim, implemented in Lua.

## Installation

```lua
    -- lazy
    {
        "xiaoyaoo11/cursorword",
        event = "VeryLazy",
        config = true,
    },
```

## Configuration

```lua
    -- default configuration
    require("stcursorword").setup({
        max_word_length = 100, -- if cursorword length > max_word_length then not highlight
        min_word_length = 1, -- if cursorword length < min_word_length then not highlight
        excluded = {
            filetypes = {
                "TelescopePrompt",
            },
            buftypes = {
                -- "nofile",
                -- "terminal",
            },
            patterns = { -- the pattern to match with the file path
                -- "%.png$",
                -- "%.jpg$",
                -- "%.jpeg$",
                -- "%.pdf$",
                -- "%.zip$",
                -- "%.tar$",
                -- "%.tar%.gz$",
                -- "%.tar%.xz$",
                -- "%.tar%.bz2$",
                -- "%.rar$",
                -- "%.7z$",
                -- "%.mp3$",
                -- "%.mp4$",
            },
        },
        highlight = {
            underline = true,
            fg = nil,
            bg = nil,
        },
    })
```

## Usage

`:Cursorword` command

| **Args**  | **Description**                             |
| --------- | ------------------------------------------- |
| `toggle`  | Toggle highlight the word under the cursor  |
| `enable`  | Enable highlight the word under the cursor  |
| `disable` | Disable highlight the word under the cursor |

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
