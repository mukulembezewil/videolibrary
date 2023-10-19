# DEPLOYING THIS APP TO NEW REPO HOME
When deploying this React App to github pages,

    2. To deploy to gh pages:

    Just follow these simple steps:

1. Install the gh-pages package (ctrl+~ to open the terminal in VS Code)
npm install gh-pages --save-dev   [or similar yarn commands]
2. In the package.json file add these lines before "build": "vite build",

"predeploy": "npm run build",
"deploy": "gh-pages -d dist",

3. In the vite.config.js file add this line before plugins: [react()],
base: "/YOUR_REPOSITORY_NAME",

Change YOUR_REPOSITORY_NAME to the name of your GitHub repository.

4. In terminal type
npm run deploy or yarn deploy
🎉 You now have a gh-pages branch in your repository and your app is deployed (you can check it under Settings -> Pages )
It took a while for the deployed app to appear in the settings.

P.S. To update your app deployment, just run the npm run deploy or yarn deploy command again.

On setting up things on the Github side visit:

https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site#creating-your-site