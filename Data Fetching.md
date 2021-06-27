# Notes-Next.js


**2 Forms of Pre-rendering**
- Static Generation (Recommended): The HTML is generated at build time and will be reused on each request. To make a page use Static Generation, either export the page component, or export getStaticProps (and getStaticPaths if necessary). It's great for pages that can be pre-rendered ahead of a user's request. You can also use it with Client-side Rendering to bring in additional data.
- Server-side Rendering: The HTML is generated on each request. To make a page use Server-side Rendering, export getServerSideProps. Because Server-side Rendering results in slower performance than Static Generation, use this only if absolutely necessary.


**getServerSideProps vs getStaticProps**
- getServerSideProps is similar to getStaticProps, but the difference is that getServerSideProps is run on every request instead of on build time.
- getServerSideProps will only render HTML on request time.
