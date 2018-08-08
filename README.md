
Ionafetch is a fast, efficient, and user-friendly library for making HTTP requests.

It also supports native ALPN negotiation in node for efficient http/2 requests!

The API was inspired by superagent, however it is much smaller and faster.
In fact, in browser, it is a mere 4.0kb.



## Some examples

```javascript
const request = require('ionafetch');

request.post('https://httpbin.org/post')
  .send({ usingGoodRequestLibrary: true })
  .then(r => console.log(r.body)); // r.body is object from json response

request.get('https://s.gc.gy/o-SNAKES.jpg')
  .then(r => fs.writeFile('download.jpg', r.body)); // r.body is buffer

request.get('https://s.gc.gy/o-SNAKES.jpg')
  .pipe(fs.createWriteStream('download.jpg')); // pipes
```

