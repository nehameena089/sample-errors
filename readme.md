# First install nodejs & then setup eslint.
1. cd boilerplate
2. npm init -y
3. npm i -D eslint eslint-config-airbnb-base eslint-plugin-import
4. Create .eslintrc.js: module.exports = { "extends": "airbnb-base" };
5. In VS Code, [Ctrl + Shift + X] Or for mac users [Cmd + Shift + X] & Search ESLint & Install ESLint
6. Restart VS Code

![EsLint](Reference - https://travishorn.com/setting-up-eslint-on-vs-code-with-airbnb-javascript-style-guide-6eb78a535ba6)

Now copy paste below lines in your .eslintrc.js

* module.exports = {
    "extends": "airbnb-base",
    "rules": {
        "camelcase": "off",
        "comma-dangle": "off",
        "newline-per-chained-call": "off",
        "class-methods-use-this": "off",
        "no-underscore-dangle": "off",
        "no-await-in-loop": "off"
    }
} *

# Guidelines for starting the app.
1. npm i in the project directory.
2. For run the server on local use ```npm run local```
3. Hit ping API http://localhost:{process.env.PORT}/test/v1/ping you will get success response.


# App Deployment and CI Pipeline
Please take note of below guidelines while forking the repository and raising pull requests
1. Branch name should not contain "/"
2. You are not allowed to modify Package.json and Dockerfile

* A CI pipleine will run after you raise a PR from your forked repo to this repo, check for the completion status of Pipeline
* Your application will be available on <your_repo_owner_name>:<your_repo>-sample-errors.demo-k8s.hypertest.co
* Hypertest Dashboard is available on http://ht-sample-errors.hypertest.demo-k8s.hypertest.co
* To Mirror Traffic: hit the request on http://hypertestco-main-sample-errors.demo-k8s.hypertest.co