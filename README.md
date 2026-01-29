# nextjs-interview-questions

**React vs Next.js**

React:
• JS library for building user interfaces
• Component-based architecture
• Virtual DOM for efficient updates
• Primarily focused on client-side rendering

Next.js:
• React framework with additional features
• Server-side rendering (SSR) and static site generation (SSG)
• File-based routing system
• Automatic code and image optimization

Key differences:
 1. Rendering: React focuses on client-side, Next.js offers SSR and SSG
 2. Routing: Next.js has built-in system, React requires additional libraries
 3. Performance: Next.js provides automatic optimizations
 4. SEO: Next.js makes it easier to create SEO-friendly applications
 5. Learning curve: React is simpler, Next.js requires additional concepts

**How Next is different from other JavaScript frameworks?**

Next.js is a JavaScript framework that is primarily designed for building React applications. Here are some key ways in which Next JS differs from other JavaScript frameworks:

Server-Side Rendering (SSR), 
Automatic Code Splitting, 
API Routes,
Built-in Image Optimization,
Easy Deployment

**What are the advantages of using Next.js over React?**

Next.js offers several advantages over React, including server-side rendering, automatic code splitting, static site generation, dynamic imports, optimized performance, and easy deployment. Additionally, Next.js supports built-in SEO and analytics, making it easier to optimize your application for search engines and track user engagement.


✅ CSR (Client-Side Rendering): Entire page built in the browser. Lightweight but slower first paint.\
✅ SSR (Server-Side Rendering): Server builds the page on each request → SEO-friendly & faster initial load.\
✅ SSG (Static Site Generation): Pages are pre-rendered at build time → blazing fast, ideal for blogs/docs.\
✅ ISR (Incremental Static Regeneration): Best of both worlds → static pages that can update on-demand without full rebuilds.


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

**Next JS client-side navigation**
It supports both traditional anchor (<a>) tags and programmatically navigating through the next/router module.

**What is the role of middleware in Next.js, and how can it be utilized?**
Middleware in Next.js allows you to run code before a request is completed, enabling functionalities like authentication, logging, or redirects. It runs on the edge, making it useful for handling tasks that need to be executed quickly and close to the user.

**How do you perform client-side data fetching in Next.js?**

import { useState, useEffect } from "react";

function Profile() {
  const [data, setData] = useState(null);
  const [isLoading, setLoading] = useState(true);

  useEffect(() => {
    fetch("/api/profile")
      .then((res) => res.json())
      .then((data) => {
        setData(data);
        setLoading(false);
      });
  }, []);

  if (isLoading) return <p>Loading...</p>;
  if (!data) return <p>No profile data</p>;

  return (
    <div>
      <h1>{data.name}</h1>
      <p>{data.bio}</p>
    </div>
  );
}
