The Occultist framework is a work in progress fullstack SSR Javascript framework will achieve many of the features touted by other modern Javascript frameworks and more. Occultist is different in that a build process can be optional, it encourages RESTful solutions, it provides fine control over HTTP caching and content type negotiation can be used to integrate specialized content types alongside Occultist's primary content type of JSON-LD.


The Occultist framework consists of the following components
<dl>
  <dt><a href="https://mithril.js.org">Mithril</a></dt>
  <dd>A small and stable vdom library which can render to HTML and control the DOM. This project is independent of the Occultist project but is an important component.</dd>
  <dt><a href="https://github.com/digitalbazaar/jsonld.js">jsonld.js</a></dt>
 <dd>A library implementing JSON-LD algorithms. This is used by Octiron to expand JSON-ld responses. jsonld.js includes a lot more functionality than Octiron requires so an implementation of JSON-LD's expansion algorithm will later be developed so this dependency can be replaced.
  <dt><a href="https://github.com/occultist-dev/octiron">Octiron</a></dt>
  <dd>A frontend framework which can traverse JSON-ld API's and map response data Mithril vdom and components. Octiron can be configured to render other content types in more optimized ways than the general use case JSON-LD responses solves. 
  <dt><a href="https://github.com/occultist-dev/occultist">Occultist</a></dt>
  <dd>A backend HTTP library inspired by Koa but also very different. This library has first class support for the HTTP accept header and can map different content types to different handlers for the same URL path. It has a powerful interface for normalizing HTTP request information to a user land cache, managing etags of dynamic data and other features which make it a different but attractive HTTP library.<dd>
  <dt><a href="https://github.com/occultist-dev/longform">Longform</a></dt>
  <dd>A markup language like Markdown but about to natively represent all HTML elements and output HTML fragments. Content rendered using Longform responses can remove the double data problem of server side rendering. It is the Octiron framework's approach to server islands, although is not limited to being treated as static content with how it integrates with Octiron.
</dl>
