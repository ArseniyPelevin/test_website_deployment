# Configure GitHub Pages in repo's Settings
- Go to the repository's 'Settings' tab
- 'Pages' section
- Select the branch (gh-pages) and folder (/ (root))

# Repository / website visibility
- Public repo: GitHub Pages work for any GitHub plan
- Private repo: GitHub Pages only work for paid plans (GitHub Pro, Team, Enterprise)

# Custom domain
- Create a CNAME file in the root of the repository with the custom domain (e.g., `www.example.com`)
- Edit _config.yml to set the custom domain:
  url: https://www.example.com
  baseurl: "" # leave empty for root domain
- Add custom domain in GitHub Pages settings

# Local Jekyll setup on Windows
- Download and install Jekyll and dependencies using RubyInstaller:
    - Download files and follow instructions from https://jekyllrb.com/docs/installation/windows/ (also available for other OS)
- Navigate to the repository folder in command prompt
- Run `jekyll serve` to build and serve the site locally
- Access the site at http://localhost:4000/Mlynarski-lab-website/
- Leave that terminal open
- Edit files in the repo folder
- Refresh the browser
