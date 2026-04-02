# Portfolio Site Setup Instructions

Follow these steps to set up your personal portfolio site using Jekyll and GitHub Pages.

## 1\. Create Your Repository

1.  Go to GitHub and create a new repository named:
    
    YourUserName.github.io
    -   Make sure **you are the owner** of this repository.
    -   Start with a **template** and choose the `CSG / PortfolioRepoTemplate`.
      
2. Clone the repository locally to your computer so you can edit it

## 2. Install Ruby + Devkit

1.  Go to [rubyinstaller.org](https://rubyinstaller.org/downloads/) and download **Ruby+Devkit 3.3.x (x64)**.
    
> [!IMPORTANT]
> The Devkit is required because it includes tools to compile native extensions.
> 
        
2.  Run the installer. At the end, you will see the `ridk install` prompt. Run it and select **all three options in order**:
    
    1.  Base installation (ensures Ruby environment is set up)
        
    2.  System update (updates internal tools)
        
    3.  MSYS2 & MINGW development toolchain (necessary compiler tools)
        

## 3. Verify Installation

Open your terminal (Command Prompt, PowerShell, or Windows Terminal) and run:
```bash
ruby \-v
```

You should see something like:

```bash
ruby 3.3.10
```

Then check `ridk`:

```bash
ridk version
```
-   If you see information about **MSYS2**, **gcc/cc**, and toolchains, your setup is ready.

## 3\. Navigate to Your Repository Folder

Change your terminal directory to your local portfolio repo:
```bash
cd "D:\\Students\\YourName\\Portfolio\\my-site"
```
## 4\. Install Jekyll Dependencies

1.  Install Bundler:
    
```bash
gem install bundler
```
> [!WARNING]
> If prompted to update RubyGems or Bundler, you can **ignore it for now**.

1.  Install all dependencies for your site:
```bash
bundle install
```
## 5\. Launch the Local Jekyll Server

Start a live preview of your site:
```bash
bundle exec jekyll serve \--livereload \--drafts \--future
```
-   `--livereload` → automatically refreshes your browser when you save changes
    
-   `--drafts` → includes draft posts
    
-   `--future` → includes posts scheduled for future dates
    

>[!WARNING]
>Every time you close your terminal, the server stops. You will need to rerun the command to preview your site again.
>

## 6\. View Your Site

Once the server is running, your terminal will display:

Server address: http://127.0.0.1:4000/

-   Open this address in your browser to view your site locally.
    
-   Any changes you make will appear live if the terminal server is running.
    

## ✅ Notes & Best Practices

-   Commit frequently as you work on your portfolio.
    
-   Keep your local server running while editing for live previews.
    
-   When finished editing locally, push your changes to GitHub to update your live site.
