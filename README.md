# github-pages-test

## How to deploy a simple React app to GitHub pages? (with routing)

### Requirements

- NodeJS 10+
- NPX and NPM installed
- GIT (obviously?)

### Steps

1. Install a React app with `npx create-react-app myapp`
2. Add router `npm i --save react-router-dom`
3. Add gh-pages `npm i --save gh-pages` 
4. See `App.js` for example React router code. For routing, use the **hashRouter**.
5. Add the following to your `package.json` in the **scripts** section (please mind the comma):

```json
    "predeploy": "npm run build",
    "deploy": "gh-pages -b gh-pages -d build"
```

6. Add the following to the `package.json` main object updating the blatant ALL-CAPS variables as necessary:

```json
    "homepage": "http://YOUR-GITHUB-USERNAME.github.io/YOUR-GITHUB-REPO-PATH",
```

7. Deploy: `npm run deploy`
8. In the repository settings in GitHub, change the **source** to `gh-pages` branch
9. You'll see your app at `http://YOUR-GITHUB-USERNAME.github.io/YOUR-GITHUB-REPO-PATH`...probably

## Note

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

### Making a Progressive Web App

This section has moved here: https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app