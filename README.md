# iframe-separate-thread-test
> Do iframe use separate thread?

No on `Chrome 81` and `Firefox 74.0`.

## topic
stackoverflow topic:
https://stackoverflow.com/questions/11510483/will-a-browser-give-an-iframe-a-separate-thread-for-javascript

## Test
```
$ http-server -g -c0 ./
Available on:
  http://127.0.0.1:8080
  http://192.168.1.4:8080
```

open `http://127.0.0.1:8080/index.html`.

## Good News
[site-isolation](https://developers.google.com/web/updates/2018/07/site-isolation) became default in Chrome 67.

Change iframe src to `http://192.168.1.4:8080/iframe.html`, iframe will **run inside another proecss** and don't block index.html page render process.

```diff
-    <iframe src="http://127.0.0.1:8080/iframe.html"></iframe>
+   <iframe src="http://192.168.1.4:8080/iframe.html"></iframe>
```

## EOF
