---
title: Installation
position: 2
content_markdown: |-

  Install fetch-mock using

  ```bash
  npm install --save-dev fetch-mock
  ```

  In most environments use one of the following in your test files

  ```js
  const fetchMock = require('fetch-mock');

  // Exposes constants that will make tests more readable
  const { fetchMock, MATCHED, UNMATCHED } = require('fetch-mock');
  ```

  Some exceptions include:

  - If your client-side code or tests do not use a loader that respects the `browser` field of `package.json` use `require('fetch-mock/es5/client')`.
  - If you need to use fetch-mock without commonjs, you can include the precompiled `node_modules/fetch-mock/es5/client-bundle.js` in a script tag. This loads fetch-mock into the `fetchMock` global variable.
  - For server side tests running in Node.js 6 or lower use<br>
  `require('fetch-mock/es5/server')`
---

