# What is a single-page application ?

SPAs have links and forms, but when users interact with them, the back-end server replies with raw data (often in JSON format) or only the relevant HTML that needs to change.

The old HTML page is retained, and changes to that page are made dynamically. All the updates are performed on the client side.

This means that the user can navigate to different parts of the application without the need to load a new page from the server.

## Multi-page applications

- A user submits a form
- The browser relays an http request
- The server receives the request
- The server prepare a response
- The server responds with html
- The html response replaces the old page

## Single-page applications

- A user submits a form
- The browser relays an http request
- The server receives the request
- The server prepare a response
- The server responds with JSON
- The JSON data is added without page reload

### JavaScript

SPAs rely extensively on JavaScript to construct and update the user interface, allowing content on a page to change dynamically.
//JavaScript handles user interactions and can suppress default browser behavior that would typically load a new HTML page.

### Routing on the Client Side

Despite the application being a single page, it can mimic the behavior of a multi-page application using client-side routing. This differs from traditional server-side routing, where each request loads a new HTML page.

### Asynchronous JavaScript and XML (AJAX)

AJAX allows applications to make HTTP requests to servers asynchronously using JavaScript. This means that the data used by an application can be delivered separately from HTML and JavaScript files themselves. Although XML (a data format) is in the name, the primary format we’ll use to exchange data is JSON.

### JavaScript Object Notation (JSON)

JSON is not only a format for configuring settings for an application, like you may be familiar with. It can also be used as a data-interchange format to structure data sent between a server and a web application.

### Client-side rendering

In a SPA, the UI for a page isn’t constructed by a server. Instead, it is constructed by the client’s browser - this is client-side rendering. JavaScript dynamically manipulates the DOM (Document Object Model) to update the UI, typically in response to user actions or AJAX operations. This leads to a more responsive user experience, similar to native applications.

### State management

SPAs maintain an application’s state on the client side. This involves tracking user interactions and data changes across the application’s lifecycle. This is critical for ensuring the UI remains consistent with the application’s state.

Often, JSON data retrieved using AJAX is stored in state. This data can be accessed, modified, or deleted. Because the application keeps the UI synchronized with state, these changes are reflected on the client without needing a server to generate new HTML.

### ECMAScript modules (ESM)

ECMAScript modules are native to JavaScript and allow code to be packaged and reused. This means code can be better structured and organized into reusable components, facilitating the development of large-scale applications without excessive code duplication.

## Advantages of SPAs over MPAs

These include improved user experience and strong support from libraries and frameworks like Angular, React, and Vue.js, which are all popular options that assist in constructing SPAs.

- More efficient server interactions: In a SPA, we are only concerned with sending and updating the needed data. When the client receives data from the server, it is stored in memory. This allows us to pass the data around the application without requesting it again, reducing the number of interactions between the client and the server.
  <br>

- Streamlined front-end development: SPAs can be easier to develop and maintain, as they often use modern front-end frameworks and libraries. This can help developers write cleaner, more organized code and use modern development tools and practices. Some of these frameworks and libraries include React, Angular, and Vue.js.
  <br>
- Easier debugging: SPAs can be easier to debug, as developers can use modern debugging tools and practices to identify and fix issues. This can reduce the time and effort required to fix bugs and problems in the application.

## Challenges of building SPAs

- Search Engine Optimization (SEO) Concerns: Search engines traditionally rely on HTML content to crawl and index web pages. SPAs dynamically load content using JavaScript, making it challenging for search engines to index the content effectively.
  <br>
- Initial Load Time: SPAs often require a larger initial load time as all the necessary assets (HTML, CSS, JavaScript) are loaded at the beginning. This can lead to slower initial page rendering compared to traditional multi-page applications.
  <br>
- Complex State Management: As a SPA grows, managing the application’s state becomes more complex. With multiple components and views, ensuring that the application behaves as expected and maintaining a consistent state across the application becomes more difficult.
  <br>
- Accessibility: Some of a SPA’s core features (dynamically updating content using JavaScript, URLs not updated server-side, etc.) pose challenges when implementing accessibility features.
