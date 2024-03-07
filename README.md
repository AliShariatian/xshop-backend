-  # [Json Server Github](https://github.com/typicode/json-server/tree/v0)

-  # [Json Server NPM](https://www.npmjs.com/package/json-server)

---

## For run Database on local for this practice:

-  `npx json-server db.json -p 8080`.

---

## For run on server (Deploy):

-  Create `backend` folder.
-  Write `npm init` or `npm init -y` in cmd on backend directory.
-  Install json-server with `npm i json-server`.
-  Create a file with name `server.js` and add below code into this file.
-  Our database file is `db.json`.

```js
// server.js
const jsonServer = require("json-server");
const server = jsonServer.create();
const router = jsonServer.router("db.json");
const middlewares = jsonServer.defaults();

server.use(middlewares);
server.use(router);
server.listen(3000, () => {
   console.log("JSON Server is running");
});
```
- In `package.json` file and in `scripts` section, add a new key and value with key: `start` and value: `node server.js`.

- Write `liara deploy` and write port `3000` in cmd.

- Finish.
  
