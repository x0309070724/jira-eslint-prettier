# 规范模板配置

## 创建项目

https://react.dev/learn/start-a-new-react-project

1. npx create-react-app jira --template typescript
2. tsconfig 配置 baseUrl 替代相对路径

## 配置 prettier

https://prettier.io/docs/en/install

1. npm install --save-dev --save-exact prettier
2. node --eval "fs.writeFileSync('.prettierrc','{}\n')"
3. create a .prettierignore file
   Pre-commit Hook:
4. npx mrm@2 lint-staged
5. 修改 package.json 里的 lint-staged 配置
   解决 prettier 和 eslint 冲突
6. npm install eslint-config-prettier -D
7. 修改 package.json 里的 eslintConfig 配置

## 规范 git commit message

https://github.com/conventional-changelog/commitlint?tab=readme-ov-file#getting-started

1. npm install --save-dev @commitlint/{config-conventional,cli}
2. echo "module.exports = {extends: ['@commitlint/config-conventional']}" > commitlint.config.js
3. npx husky add .husky/commit-msg 'npx --no -- commitlint --edit ${1}'

## 配置 mock 功能，json-server（json-server 遵循 restful 规范，所以也可以选择 mock.js）

1. npm install json-server -D
2. 新建 \_\_json_server_mock/db.json 文件
3. 修改 package.json scripts
