LONAI PORTFOLIO REFRESH

Files in this package:
- src/index.html: replacement portfolio page
- src/style.css: replacement responsive styling
- .github/workflows/deploy.yml: GitHub Pages workflow that publishes ./src

INSTALL FROM YOUR PROJECT ROOT

1. Back up your current files:
   cp src/index.html src/index.html.backup
   cp src/style.css src/style.css.backup

2. Copy the replacement files from this package into your Project-Homepage folder,
   preserving the src/ and .github/workflows/ folder structure.

3. Keep your existing image assets in src/:
   sonGohan.jpg, Gohan.jpeg, phone.svg, email.svg, etc.
   This redesign uses ./sonGohan.jpg. It does not require the other assets.

4. Commit and push:
   git add src/index.html src/style.css .github/workflows/deploy.yml
   git commit -m "Polish portfolio and add project showcase"
   git push origin main

5. In GitHub: Project-Homepage > Settings > Pages > Build and deployment,
   select Source: GitHub Actions.

6. Check the Actions tab for a successful "Deploy portfolio to GitHub Pages" run.

PROJECT LINKS

The cards link to public repositories that were discoverable under your GitHub account.
Restaurant Page and Smart E-commerce App are shown as local-workspace projects because
I could not verify matching public repositories for those folder names. Add their
repository URLs to the HTML when you publish them.

NOTE

The workflow publishes the contents of src/ directly. It does not run Webpack.
Your current Webpack configuration still references the deleted src/template.html;
that is separate from this static GitHub Pages deployment.
