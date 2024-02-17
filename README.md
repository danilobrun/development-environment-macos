# development-environment-macos

### Which terminal do I use?

```jsx
echo $SHELL
echo $0
ps -p $$
```

- Install Oh My ZSH + HomeBrew
  ```jsx
  Oh My ZSH
  sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"\n\n

  HomeBrew
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

  NVM
  curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.2/install.sh | bash
  nvm install node
  cat ~/.zshrc
  ls ~/.nvm

  Fix NodeJS
  npm install node-gyp

  # Install with brew
  brew install wget
  ```
- Install zsh syntax highlighting + zsh auto suggestion
  # Step by step
  ```
  # zsh sytanx highlighting
  https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md
  git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

  # zsh auto suggestions
  https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md#oh-my-zsh
  git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

  # zsh spaceship-prompt
  https://github.com/spaceship-prompt/spaceship-prompt
  git clone https://github.com/spaceship-prompt/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1

  # after clone all repos edit zshrc profile file -> ˜/.zshrc
  nano ˜/.zshrc
  nano: control + w (to search plugins)
  edit -> plugins=(git zsh-syntax-highlighting zsh-autosuggestions)
  nano: control + w (to search ZSH_THEME)
  edit -> ZSH_THEME="spaceship"
  control + o (to save file)
  control + x (to exit file)

  # You must have create symlink (link simbólico, atalho) for spaceship
  ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"

  ```
  # More info about zsh (syntax, auto suggestions, spacheship-prompt) bellow 👇🏼
  ### [Oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh) sytanx highlighting
  1. Clone this repository in oh-my-zsh's plugins directory:

     ```
     git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
     ```

  2. Activate the plugin in `~/.zshrc`:

     ```
     plugins=( [plugins...] zsh-syntax-highlighting)
     ```

  3. Restart zsh (such as by opening a new instance of your terminal emulator).
  ## Oh My Zsh auto suggestions
  1. Clone this repository into `$ZSH_CUSTOM/plugins` (by default `~/.oh-my-zsh/custom/plugins`)

     ```
     git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
     ```

  2. Add the plugin to the list of plugins for Oh My Zsh to load (inside `~/.zshrc`):

     ```
     plugins=(
         # other plugins...
         zsh-autosuggestions
     )
     ```

  3. Start a new terminal session.
  ### Spaceship-prompt ZSH
  https://github.com/spaceship-prompt/spaceship-prompt
  Oh-My-Zsh
  Clone this repo:
  ```
  git clone https://github.com/spaceship-prompt/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1
  ```
  Symlink `spaceship.zsh-theme` to your oh-my-zsh custom themes directory:
  ```
  ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"
  ```
  Set `ZSH_THEME="spaceship"` in your `.zshrc`.
  https://www.youtube.com/watch?v=bs1-Wxb_KIc&t=0s
- JetBrainsMono Fonts install 🔠
  1. Baixar as fontes do site official da jet brains fonto mono
  2. Dentro do arquivo /JetBrainsMono/fonts/ttf (contém todas as fontes dentro)
  3. Selecionar todas ctrl+a aperta enter para abrir todas de uma vez e instalar
  4. Configurando a fonte no vscode → ctr + , (settings) → editor font family: JetBrains Mono por padrão do vs code vem → Menlo, Monaco, 'Courier New', monospace
  5. Por padrão o terminal do macOS vem com essa configuração podemos alterar a fonte para a fonte do JetBrains Mono
  ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/66e12046-474f-4770-8a2f-8311baa71251/fe1093ab-1cec-419b-983b-b6218174137c/Untitled.png)
