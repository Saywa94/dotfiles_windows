# Dotfiles for my windows setup

Container:
- git configuration
- vim configuration
- Windows Terminal configuration
- windows custom commands

Programs required:
- Git
- Cmder
- Vscode
- Windows Terminal
- Cascadia Mono (font)

For dotfiles to work create a symlink to the user profile directory:

    cd %USERPROFILE%
    mklink .gitignore .dotfiles/.gitignore
    mklink .vimrc .dotfiles/.virmc

    <!-- for Windows terminal configuration -->
    cd 'C:\Users\aywac\AppData\Local\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState'
    mklink setting.json %USERPROFILE%\.dotfiles\settings.json
    mv setting.json settings.json

That is assuming `.dotfiles` is in your `%USERPROFILE%` directory.