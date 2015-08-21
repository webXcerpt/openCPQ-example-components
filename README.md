openCPQ Components
==================
*A demo example for [openCPQ](https://github.com/webXcerpt/openCPQ).*

This demo lists all available primitive and compound components from openCPQ, as well as some application-specific components.


Running the Components in the Web
---------------------------------

The configurator can be started from http://opencpq.webxcerpt.com/examples/components/.

Building and Serving the Configurator
-------------------------------------

The commands below require that you have the programs
[`git`](https://git-scm.com/), `node` (actually the `node` program
coming with [`iojs`](https://iojs.org/en/index.html) and `npm` (also
coming with `iojs`) installed and in your "PATH".

Run the following commands to build and serve the configurator:

```sh
$ git clone https://github.com/webXcerpt/openCPQ-example-components.git
$ cd openCPQ-example-components
$ npm install
$ npm run dev-server
```

Now point your browser to
[http://localhost:8080/webpack-dev-server/index.html](http://localhost:8080/webpack-dev-server/index.html).
The development server will observe your changes to the code, rebuilding
the application as needed and reloading it in your browser.  This is
quite comfortable for configurator development.  You can stop the
development server with Control-C.

To build the application in directory `./dst/` in "production mode", run

```sh
$ npm run build
```

(still from within `openCPQ-example-components`).

To deploy that build via FTP to your HTTP server you can run

```sh
$ npm run deploy
```

This requires that you have a file `deployment.json` of the form

```json
{
  "host": "...",
  "user": "...",
  "password": "...",
  "folder": "..."
}
```

providing the FTP location and credentials for the deployment.
