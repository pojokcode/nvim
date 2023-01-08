## HOME

![home!](img/home.png)

## PHP

![LARAVEL!](img/laravel.jpeg)

## JAVA

![JAVA!](img/Spring_boot_code.jpeg)
![JAVA!](img/terminal_spring_boot.jpeg)

# Panduan Install Dan Konfigurasi NeoVim

## Kebutuhan Dasar

1. Install Neovim 8.0+ https://github.com/neovim/neovim/releases/tag/v0.8.1
2. C++ (windows) Compiler https://www.msys2.org/
3. GIT https://git-scm.com/download/win
4. NodeJs https://nodejs.org/en/
5. Ripgrep https://github.com/BurntSushi/ripgrep
6. Lazygit https://github.com/jesseduffield/lazygit
7. Nerd Font https://github.com/ryanoasis/nerd-fonts
8. Windows Terminal (Windows) https://apps.microsoft.com/store/detail/windows-terminal/9N0DX20HK701?hl=en-id&gl=id
9. Powershell (windows) https://apps.microsoft.com/store/detail/powershell/9MZ1SNWT0N5D?hl=en-id&gl=id

## Panduan Windows

- Pastikan sudah menginstall kebutuhan dasar diatas
- Jalankan Script Dibawah pada Powershell

```
git clone https://github.com/pojokcodeid/nvim.git "$env:LOCALAPPDATA\nvim"
nvim
```

## Panduan Linux (Debian Based)

1.  Pastikan Acess Administrator

```
visudo
[nama user] ALL=(ALL:ALL) ALL
[nama user] ALL=(ALL) NOPASSWD:ALL
```

2. Install Neovim

```
sudo apt-get install wget
mkdir download
cd download
wget https://github.com/neovim/neovim/releases/download/v0.8.1/nvim-linux64.deb
sudo apt-get install ./nvim-linux64.deb
nvim --version
```

3. Check GCC

```
gcc --version
```

4. Install NodeJS

```
sudo apt-get install curl
sudo apt install build-essential libssl-dev
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
source ~/.bashrc
nvm install 18.13.0
node --version
npm --version
```

5. Install unzip, ripgrep

```
sudo apt-get install unzip
sudo apt-get install ripgrep
```

6. Install lazygit

```
LAZYGIT_VERSION=$(curl -s "https://api.github.com/repos/jesseduffield/lazygit/releases/latest" | grep '"tag_name":' |  sed -E 's/.*"v*([^"]+)".*/\1/')
curl -Lo lazygit.tar.gz "https://github.com/jesseduffield/lazygit/releases/latest/download/lazygit_${LAZYGIT_VERSION}_Linux_x86_64.tar.gz"
sudo tar xf lazygit.tar.gz -C /usr/local/bin lazygit
lazygit --version
```

7. Install Git

```
sudo apt-get install git
git --version
```

8.  Clone Config

```
git clone https://github.com/pojokcodeid/nvim.git ~/.config/nvim
```

## Setting LSP dan Treesitter

### Config LSP - Cari file nvim/lua/user/lsp/mason.lua

- Tambahkan pada bagian berikut

```
local servers = {
	"sumneko_lua",
	"cssls",
	"html",
	"tsserver",
	"pyright",
	-- "bashls",
	"jsonls",
	-- "yamlls",
	-- "jdtls",
	"emmet_ls",
	"intelephense",
}
```

- Rujukan Lnguage Support <br>
  https://github.com/williamboman/mason.nvim/blob/main/PACKAGES.md

### Comfig Treesitter Cari file nvim/lua/user/treesitter.lua

- Tambahkan Pada Bagian berikut

```
ensure_installed = {
		"bash",
		"c",
		"javascript",
		"json",
		"lua",
		"python",
		"typescript",
		"tsx",
		"css",
		"rust",
		"java",
		"yaml",
		"markdown",
		"markdown_inline",
	}, -- one of "all" or a list of languages
```

- Rujukan Language Support <br>
  https://github.com/nvim-treesitter/nvim-treesitter#supported-languages

## Seting Bahasa Pemprograman

- https://youtube.com/playlist?list=PLhzwHCJWMbnvhPy0wqZGVBRUEAgS93iuk

## List Plugins

- <a href="https://github.com/wbthomason/packer.nvim">Packer </a>
- <a href="https://github.com/nvim-lua/plenary.nvim">Plenary </a>
- <a href="https://github.com/windwp/nvim-autopairs">Nvim-Autopairs </a>
- <a href="https://github.com/numToStr/Comment.nvim">Comment.nvim</a>
- <a href="https://github.com/JoosepAlviste/nvim-ts-context-commentstring">nvim-ts-context-commentstring</a>
- <a href="https://github.com/nvim-tree/nvim-web-devicons">nvim-web-devicons</a>
- <a href="https://github.com/nvim-tree/nvim-tree.lua">nvim-tree.lua</a>
- <a href="https://github.com/akinsho/bufferline.nvim">bufferline.nvim</a>
- <a href="https://github.com/moll/vim-bbye">vim-bbye</a>
- <a href="https://github.com/akinsho/toggleterm.nvim">toggleterm.nvim</a>
- <a href="https://github.com/lewis6991/impatient.nvim">impatient.nvim</a>
- <a href="https://github.com/lukas-reineke/indent-blankline.nvim">indent-blankline.nvim</a>
- <a href="https://github.com/goolord/alpha-nvim">alpha-nvim</a>
- <a href="https://github.com/folke/which-key.nvim">which-key.nvim</a>
- <a href="https://github.com/folke/tokyonight.nvim">tokyonight.nvim</a>
- <a href="https://github.com/hrsh7th/nvim-cmp">nvim-cmp</a>
- <a href="https://github.com/hrsh7th/cmp-buffer">cmp-buffer</a>

## key lazygit

<a href="https://github.com/jesseduffield/lazygit/blob/master/docs/keybindings/Keybindings_en.md?fbclid=IwAR3BogewbYeP0PbPY1pewCkq2c3PKua3eHi-00rHpdSdz9gSKrY71Pv10u4" target="_blank">Key Lazygit</a>

## Terima Kasih

https://github.com/LunarVim/Neovim-from-scratch <br>
https://github.com/AstroNvim/AstroNvim
