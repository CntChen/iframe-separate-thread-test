# iframe-separate-thread-test
> Do iframe use separate thread?

No on `Chrome 81` and `Firefox 74.0`.

## topic
stackoverflow topic:
https://stackoverflow.com/questions/11510483/will-a-browser-give-an-iframe-a-separate-thread-for-javascript

## Test
```
$ http-server -g -c0 ./
```

open `http://127.0.0.1:8080/index.html`.

## EOF
