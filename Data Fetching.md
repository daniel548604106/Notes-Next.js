# Notes-Next.js


**2 Forms of Pre-rendering**
- Static Generation (Recommended): The HTML is generated at build time and will be reused on each request. To make a page use Static Generation, either export the page component, or export getStaticProps (and getStaticPaths if necessary). It's great for pages that can be pre-rendered ahead of a user's request. You can also use it with Client-side Rendering to bring in additional data. (靜態頁面是在 build-time 時就產生，伺服器收到 request 時重複使用這些已經生成好的靜態頁面。)
- Server-side Rendering: The HTML is generated on each request. To make a page use Server-side Rendering, export getServerSideProps. Because Server-side Rendering results in slower performance than Static Generation, use this only if absolutely necessary. (伺服器每次收到請求時在產生對應的靜態頁面。)


**getServerSideProps vs getStaticProps**
- getServerSideProps is similar to getStaticProps, but the difference is that getServerSideProps is run on every request instead of on build time.
- getServerSideProps will only render HTML on request time, so only ssr.js with a asynv getServerSideProps will be generated, which is called when request is made to the page,  instead of both ssr.html and ssr.js (每一個產生好的 HTML 頁面都會伴隨部分的 JavaScript，當一個頁面被瀏覽器載入後，這些 JavaScript 的程式碼會執行，以讓頁面能夠帶有完整的互動功能（這個過程稱作hydration）)


**getStaticPaths**

Common error
- A required parameter(photo) was not provided as a string in getStaticPaths for [photo] : this usually results from not returning the params with the same name as what we've named for the path . (ex. [photo] , but we returned params: { id: photo.id }). Make sure it has to be the same name.
- An error may occur when you're passing parameters that's not of type string, make sure to put that on note.
