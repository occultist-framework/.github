# Occultist.dev

Occultist.dev is a work in progress fullstack SSR Javascript framework that can achieve many of the features popular by other modern Javascript frameworks but with its own spin on them. Occultist.dev leans into RESTful solutions, favours control of HTTP caching and content type negotiation over static bundlers.


The Occultist.dev project consists of the following components.
<dl>
  <dt><a href="https://mithril.js.org">Mithril</a></dt>
  <dd>A small and stable vdom library which can render to HTML and control the DOM. This project is independent of the Occultist.dev project but is an important component.</dd>
  <dt><a href="https://github.com/digitalbazaar/jsonld.js">jsonld.js</a></dt>
 <dd>A library implementing JSON-LD algorithms. This is used by Octiron to expand JSON-LD responses. jsonld.js includes a lot more functionality than Octiron requires so an implementation of JSON-LD's expansion algorithm will later be developed so this dependency can be replaced.
  <dt><a href="https://github.com/occultist-dev/octiron">Octiron</a></dt>
  <dd>A frontend framework which can traverse JSON-LD API's and map response data to Mithril vdom and components. Occultist can be configured to render other content types in more optimized ways than the general use case JSON-LD responses solves. 
  <dt><a href="https://github.com/occultist-dev/occultist">Occultist</a></dt>
  <dd>A backend HTTP library inspired by Koa but also very different. This library has first class support for the HTTP accept header and can map different content types to different handlers for the same URL path. It has a powerful interface for normalizing HTTP request information to a user land cache, managing etags of dynamic data and other features which make it a different but attractive HTTP library.<dd>
  <dt><a href="https://github.com/occultist-dev/longform">Longform</a></dt>
  <dd>A markup language like Markdown but able to natively represent all HTML elements and output HTML fragments. Content rendered using Longform responses can remove the double data problem of server side rendering for content wrapping dynamic Mithril vdom and the static markup rendered by the dynamic Mithril vdom.
</dl>
