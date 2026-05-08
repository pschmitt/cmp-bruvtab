# cmp-bruvtab

Browser tab content content completion for
[nvim-cmp](https://github.com/hrsh7th/nvim-cmp).

# Requirements

- [neovim](https://github.com/neovim/neovim)
- [nvim-cmp](https://github.com/hrsh7th/nvim-cmp)
- [BruvTab](https://github.com/pschmitt/bruvtab)

# Installation (packer.nvim)

```lua
use {
  'pschmitt/cmp-bruvtab',
  requires = "hrsh7th/nvim-cmp",
}
```

# Configuration

```lua
require('cmp').setup({
  sources = {
    { name = 'bruvtab' }
  }
})
```

# LunarVim Configuration

```lua
lvim.plugins = {
  {
    "pschmitt/cmp-bruvtab"
    requires = "hrsh7th/nvim-cmp",
    event = "InsertEnter",
    setup = function()
      table.insert(lvim.builtin.cmp.sources, { name = "bruvtab" })
      lvim.builtin.cmp.formatting.source_names.bruvtab = "(BRUVTAB)"
    end
  },
}
```lua
