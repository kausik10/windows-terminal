    # Custom Windows Terminal Theme

    ## Project Description:
    I am tired of boring PowerShell and terminal looks, especially after shifting to a Windows-based working environment with WSL enabled. This project provides a custom theme to bring the aesthetic appeal of Linux environments, including NerdFonts and other customizable features.

    ## Installation:

    
        1. **Install Windows Terminal:** Install "Windows Terminal" from your Microsoft Store.
        1. **Install NerdFonts:** Install "NerdFonts" from their <a href="https://github.com/ryanoasis/nerd-fonts/releases" target="_blank" rel="noopener noreferrer">GitHub repository</a>. Personally, I prefer FiraCode Mono.
        <ol type="a">
            1. Extract the files, right-click, and select "Install" for the fonts. Install these fonts in any location of your OS.
        
        **Install oh-my-posh:** Follow the instructions on the [oh-my-posh website](https://ohmyposh.dev/docs/installation/windows) or run the following commands in your Windows Terminal:
        
            * <button onclick="copyToClipboard('winget install JanDeDobbeleer.OhMyPosh -s winget')">Install oh-my-posh and Themes</button>
            * <button onclick="copyToClipboard('winget upgrade JanDeDobbeleer.OhMyPosh -s winget')">Update oh-my-posh (Optional)</button>
        
        **Find and Apply Themes:** Run the following commands:
        
            * <button onclick="copyToClipboard('oh-my-posh init pwsh --config \'$env:POSH_THEMES_PATH\jandedobbeleer.omp.json\' | Invoke-Expression')">Get Default Theme</button>
            * <button onclick="copyToClipboard('Get-PoshThemes')">List Available Themes</button>
            * <button onclick="copyToClipboard('oh-my-posh init pwsh --config \'C:\Users\ASUS\AppData\Local\Programs\oh-my-posh\themes\cinnamon.omp.json\' | Invoke-Expression')">Apply Custom Theme</button>
        
        **Ensure Persistency:** Run the following commands:
        
            * <button onclick="copyToClipboard('New-Item -Path $PROFILE -Type File -Force')">Create Profile</button>
            * <button onclick="copyToClipboard('notepad $PROFILE')">Open Profile</button>
            * <button onclick="copyToClipboard('oh-my-posh init pwsh --config \'C:\Users\ASUS\AppData\Local\Programs\oh-my-posh\themes\cinnamon.omp.json\' | Invoke-Expression')">Apply Theme in Profile</button>
        
        **Restart Terminal:** Restart the terminal to see the changes.
    

    If you want to know more, follow oh-my-posh's official documentation: [oh-my-posh Documentation](https://ohmyposh.dev/docs/).

    
        function copyToClipboard(text) {
            navigator.clipboard.writeText(text);
            alert("Copied to clipboard: " + text);
        }
    




