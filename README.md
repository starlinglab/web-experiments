Site is available at https://starlinglab.github.io/web-experiments/

## How to Embed a WACZ File
See the instructions on the [replayweb.page docs](https://replayweb.page/docs/embedding)

**Basic Steps**
1. Host the WACZ files somewhere. An S3 bucket, or whatever your site uses
2. If necessary (if you aren't hosting your wacz files on the same domain as your site) [set up CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)
3. Embed the HTML
   ```html
   <script src="https://cdn.jsdelivr.net/npm/replaywebpage@1.8.1/ui.js"></script>
   <replay-web-page source="https://replayweb.page/docs/assets/tweet-example.wacz"
    url="https://oembed.link/https://twitter.com/webrecorder_io/status/1565881026215219200"></replay-web-page>
   ```
The `source` is the URL where the WACZ files is hosted, the `url` is the webpage within the WACZ file you want your viewer to display as the landing page
4.Add the service worker somewhere on your site and reference it in your HTML page

## How to Embed a C2PA file
