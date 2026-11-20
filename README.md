# blog-redirect

Serves `blog.lobocv.com` on GitHub Pages and sends every path to the same path on
[www.lobocv.com](https://www.lobocv.com) (source: `lobocv/blog`).

- `index.html` and `404.html` redirect in the browser, keeping the path, query and hash.
  GitHub Pages can't send real 301s, so this is the closest it gets
- Feed readers don't run JavaScript, so `index.xml` and `posts/index.xml` are copies
  of the live feeds, refreshed daily by `.github/workflows/sync-feeds.yml`
