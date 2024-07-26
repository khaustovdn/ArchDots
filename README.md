# ArchDots

## NeoVim

### Instalation
```
bash (curl -s https://raw.githubusercontent.com/lunarvim/lunarvim/master/utils/installer/install.sh | psub)
lvim ~/.config/fish/config.fish {
  set -gx PATH ~/.local/bin $PATH
}
```

### Config
```
vim.opt.cmdheight = 2
vim.opt.guifont = "monospace:h17"
vim.opt.shiftwidth = 2
vim.opt.tabstop = 2
vim.opt.relativenumber = true
vim.opt.wrap = true

lvim.colorscheme = "dracula"

vim.opt.foldmethod = "expr"
vim.opt.foldexpr = "nvim_treesitter#foldexpr()"

lvim.autocommands = {
  {
    { "ColorScheme" },
    {
      pattern = "*",
      callback = function()
        vim.api.nvim_set_hl(0, "Normal", { bg = "#212121", underline = false, bold = true })
      end,
    },
  },
}

lvim.plugins = {
  { "lunarvim/colorschemes" },
  { "dracula/vim" },
}
```

## FireFox
```
https://github.com/cascadefox/cascade.git
```

## Yay
```
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
```
