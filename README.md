# Vue Deafult App

In this task you will create a new Vue.js app and deploy it to GitHub Pages.

Here is a shor instruction:

1. Fork the repo and clone the forked one
1. Ensure that your `node -v` fits [Prerequisites](https://vuejs.org/guide/quick-start.html#creating-a-vue-application)
1. Open the project folder and init new Vue.js app inside it:
    ```shell
    npm create vue@latest
    ```
    - use `.` as a project name to create an app in current folder
    - allow to delete files in current folder
    - enter `vue_default-app` as a package name
    - answer `No` to all the next questions
1. Instals dependencies `npm i`
1. Run the project `npm run dev`
1. Add `base` to `vite.config.js`
    ```js
    base: '/vue_default-app/',
    ```
1. Create and switch to the `develop` branch
    ```shell
    git co -b develop
    ```
1. Save the changes and push to the repo
    ```shell
    git add .
    git ci -m 'create default Vue.js App'
    git push -u origin develop
    ```
1. Create a new file `.github/workflows/static.yml` with the content from [GitHub Pages section](https://vitejs.dev/guide/static-deploy.html#github-pages)
1. Add `'develop'` next to `'main'` into the `on:` -> `push:` -> `branches` array:
    ```yaml
    on:
      # Runs on pushes targeting the default branch
      push:
        branches: ['main', 'develop']
    ```
1. Save chnages and push the `develop` branch to the repo
