# Configure GitHub Pages in repo's Settings
- Go to the repository's `Settings` tab
- `Pages` section
- Select the branch (`gh-pages`) and folder (`/ (root)`)

# Repository / website visibility
- Public repo: GitHub Pages work for any GitHub plan
- Private repo: GitHub Pages only work for paid plans (GitHub Pro, Team, Enterprise)

Possible workarounds:
- Website code in a public repository
- Website code in a private repository, build static site locally, publish static files to a public repository and use GitHub Pages from that repository
- Website code in a private repository, build static site locally, publish static files to a custom domain without GitHub Pages

# Custom domain
- Create a CNAME file in the root of the repository with the custom domain (e.g., `www.example.com`)
- Edit _config.yml to set the custom domain:
  `url: https://www.example.com`
  `baseurl: ""` # leave empty for root domain
- Add custom domain in GitHub Pages settings

# Local Jekyll setup on Windows
See updates immediately without waiting for GitHub Pages to build and deploy the site
- Download and install Jekyll and dependencies using RubyInstaller:
    - Download files and follow instructions from https://jekyllrb.com/docs/installation/windows/ (also available for other OS)
- `cd path/to/repo`
- `jekyll serve` to build and serve the site locally
- Access the site at http://localhost:4000/Mlynarski-lab-website/
- Leave that terminal open
- Edit files in the repo folder
- Refresh the browser

# Build static site
- `cd path/to/repo`
- `jekyll build` to build the static site in the `_site` folder

To see build output locally:
- Edit _config.yml to set `url: ""` and `baseurl: ""`
- `cd _site`
- `python -m http.server 8000`
- http://localhost:8000/

To publish only the static pages on a public repository with GitHub Pages:
- Edit _config.yml to set `url: https://Mlynarski-Group.github.io` and `baseurl: /Mlynarski-lab-website`
- Initialize a new Git repository in the `_site` folder
- Push the changes to the repository

To publish on a custom domain without GitHub Pages:
- Edit _config.yml to set `url: https://www.example.com` and `baseurl: ""`
- Upload the contents of the `_site` folder to the custom domain hosting provider (e.g., using FTP or GitHub Pages)