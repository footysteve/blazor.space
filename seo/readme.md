
I've been thinking about how SEO would work with Blazor/WebAssembly so did a little investigation.

First I tried some seo analysis tools which gave scores ranging from 0 to 73 / 100 depending. This confirmed what I'd been thinking - namely that there might be some issues indexing wasm apps.
Then I indexed blazor.space with the "Fetch as Google" tool in the google search concole which gives a good idea of what a search engine sees.

This is the result of the indexing: 
![Google site indexing](https://github.com/footysteve/blazor.space/blob/master/images/blazor-seo.jpg)

You can see google isn't able to glean much about content. It only sees the index file and not much else.

So I'm going to see if I can build some middleware to solve this.

I'm currently looking at the Blazor Extensions UseBlazor. A starting point perhaps, it calls UseStaticFiles a couple of times which is what I think I'm interested in so seems a reasonable place to start.



