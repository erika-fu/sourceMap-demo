# sourcemap-demo

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

## GitHub Actions CI/CD

The workflow in `.github/workflows/ci-cd.yml` runs automatically:

- Pull requests targeting `main`: install dependencies, lint, and build.
- Pushes to `main`: run CI and deploy the generated `dist` directory to GitHub Pages.
- Manual runs: available from the Actions tab.

### GitHub configuration

1. Create a GitHub repository and push this project to its `main` branch.
2. Open the repository's **Settings > Pages**.
3. Under **Build and deployment**, set **Source** to **GitHub Actions**.
4. Open the **Actions** tab and verify that the **CI/CD** workflow succeeds.
5. After deployment, open the URL shown in the `Deploy to GitHub Pages` job.

The workflow automatically uses `/<repository-name>/` as the production public
path. Repositories named `<owner>.github.io` use `/` instead.
