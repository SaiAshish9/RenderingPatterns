```
Rendering Patterns:

1. Client Side Rendering (CSR)
2. Server Side Rendering (CSR)
3. Static Site Generation (SSG)
  a. With Data
  b. Without Data
  b.1. Fetch Data On Client
  b.2. No Data
5. Incremental Static Re-Generation (iSSG)
```

```
Pre Render:
```

<img width="686" alt="Screenshot 2024-08-19 at 10 03 34 AM" src="https://github.com/user-attachments/assets/a514ebc5-ba75-4e05-bf85-2489a07e53c5">

```
No Pre Rendering (Simple React Application): HTML doesn't contain any pre rendered content, js file at initial page load. If JS is heavy, we can see the effect of loading.
```

```
Pre Rendered Application (Next.js Application): 
```

```
By default if we don't use getServerSideProps in Next, it's going to be a CSR. 

Prerender typically refers to the process of rendering content before it is delivered to the user. This is common in web development, where it can improve performance and SEO by generating HTML on the server side rather than relying on client-side rendering.

In a prerendered web application:

Static Site Generation (SSG): Pages are rendered as static HTML files at build time. This approach is used by frameworks like Next.js and Gatsby, where content is generated once and served to all users. It’s ideal for content that doesn’t change often.

Server-Side Rendering (SSR): The server renders the page whenever a request is made, ensuring that the user receives a fully rendered page without waiting for the client-side JavaScript to execute. This can be beneficial for dynamic content that changes frequently.

Hybrid Approaches: Some frameworks allow combining both SSG and SSR, rendering some parts of the app statically and others dynamically based on the needs.

Prerendering can significantly enhance performance, especially in cases where initial load times are critical, such as with mobile users or SEO considerations.
```


```
CSR
```

```
if we use [...].map => <>, elements will be rendered on client and in network tab, html file we won't be able to view data on the intial loaded HTML file.
Crawlers read data from server, hence this part is not SEO friendly. Most react apps poor in SEO.
```


```
Using getServerSideProps in js file of Next.js application, we can include the elements in our initial loaded html file
```

```


