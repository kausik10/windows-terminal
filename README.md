# Custom Windows Terminal Theme

## Project Description:
I am tired of boring PowerShell and terminal looks, especially after shifting to a Windows-based working environment with WSL enabled. This project provides a custom theme to bring the aesthetic appeal of Linux environments, including NerdFonts and other customizable features.

## Installation:

```bash
npx create-next-app --example blog-starter blog-starter-app
```

```bash
yarn create next-app --example blog-starter blog-starter-app
```

```bash
pnpm create next-app --example blog-starter blog-starter-app
```

    
1. **Install Windows Terminal:** Install "Windows Terminal" from your Microsoft Store.
1. **Install NerdFonts:** Install "NerdFonts" from their <a href="https://github.com/ryanoasis/nerd-fonts/releases" target="_blank" rel="noopener noreferrer">GitHub repository</a>. Personally, I prefer FiraCode Mono.
        <ol type="a">
1. Extract the files, right-click, and select "Install" for the fonts. Install these fonts in any location of your OS.
        
**Install oh-my-posh:** Follow the instructions on the [oh-my-posh website](https://ohmyposh.dev/docs/installation/windows) or run the following commands in your Windows Terminal:
        
* Install oh-my-posh and Themes
```bash
winget install JanDeDobbeleer.OhMyPosh -s winget
```
* Update oh-my-posh (Optional)
```bash
winget upgrade JanDeDobbeleer.OhMyPosh -s winget
```
        
**Find and Apply Themes:** Run the following commands:

* Get Default Themes Downloaded
```bash
oh-my-posh init pwsh --config \'$env:POSH_THEMES_PATH\jandedobbeleer.omp.json\' | Invoke-Expression
```

* List all the available themes
```bash
Get-PoshThemes
```

* Apply Custom Theme
From the list of available themes, select a custom theme and apply it. It is usually stored in `C:\Users\{YOUR_DEVICE}\AppData\Local\Programs\oh-my-posh\themes\` folder.
Change the `YOUR_DEVICE` to a location in your device. In my case it is `ASUS`. And for demostration, I have used the `cinnamon` theme. Feel free to use any theme of your choice
```bash
oh-my-posh init pwsh --config \'C:\Users\ASUS\AppData\Local\Programs\oh-my-posh\themes\cinnamon.omp.json\' | Invoke-Expression
```
        
**Ensure Persistency:** Run the following commands:

To ensure theme exists on rebooting terminal / powershell

* Create Profile
```bash
New-Item -Path $PROFILE -Type File -Force
```

* Open Profile
```bash
notepad $PROFILE
```

* Apply Theme in Profile for Consistency
Again don't forget to change the `path` of your `device`. We have just piped the `Invoke-Expression` from the above code.
```bash
oh-my-posh init pwsh --config \'C:\Users\ASUS\AppData\Local\Programs\oh-my-posh\themes\cinnamon.omp.json\' | Invoke-Expression
```
        
**Restart Terminal:** Restart the terminal to see the changes.
    

If you want to know more, follow oh-my-posh's official documentation: [oh-my-posh Documentation](https://ohmyposh.dev/docs/).





