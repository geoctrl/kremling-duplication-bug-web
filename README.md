# kremling-duplication-bug-web

This repo is to show that the "invalid hook call" issue doesn't exist in a web app.

Steps:

1. clone repo
2. run `yarn`
3. add this to `node_modules/react-dom/index.js`:

```javascript
window.React1 = require('react');
```

4. run `yarn start`
5. go to `localhost:8080`
6. open dev tools - console.log should output: `true`