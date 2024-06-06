# nextjs-interview-questions

**How Next is different from other JavaScript frameworks?**

Next.js is a JavaScript framework that is primarily designed for building React applications. Here are some key ways in which Next JS differs from other JavaScript frameworks:

Server-Side Rendering (SSR), 
Automatic Code Splitting, 
API Routes,
Built-in Image Optimization,
Easy Deployment

**What are the advantages of using Next.js over React?**

Next.js offers several advantages over React, including server-side rendering, automatic code splitting, static site generation, dynamic imports, optimized performance, and easy deployment. Additionally, Next.js supports built-in SEO and analytics, making it easier to optimize your application for search engines and track user engagement.

**What do you mean by SSR?**

This is server-side rendering. This enables rendering on the server a client-side page app, and then we can send that rendered page to that client. These pages get loaded faster as the browser gets access to them sooner.

**What is client-side rendering?**

Client-side rendering (CSR) is a rendering technique where the web page’s content is generated and displayed on the client-side (i.e., the browser) using JavaScript.

**How do you pass data between pages in a Next.js application?**

Next.js provides several ways to pass data between pages in a Next.js application, including URL query parameters, the Router API, and state management libraries like Redux or React Context. You can also use the getServerSideProps function to fetch data on the server and pass it as props to the page component.

**Difference between getServerSideProps and getStaticProps functions in Next.js?**

The getServerSideProps function is used to fetch data on the server at runtime for server-side rendering, while the getStaticProps function is used to fetch data at build time for static site generation.

**Server Component VS Client Component**

![Nextjs](https://github.com/Sathyaraj-dev/nextjs-interview-questions/assets/57762726/09e28241-1e93-4149-b1eb-1d503b543206)

**Route Handlers:** 
Use Route Handlers to access your backend resources from Client Components. But do not call Route Handlers from Server Components to avoid an additional server request.
