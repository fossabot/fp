# fp

[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FIoTcat%2Ffp.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2FIoTcat%2Ffp?ref=badge_shield)

Let fp work with Cookie, cross-domain, make it stable and reliable!


## What is fp?
fp is a concise web front-end solution to generate an unique 'fingerprint' for each visitor basing on visitor's device and browser.


## Quick start

[Click here to see how it works!](https://fp.yimian.xyz/demo.html)


## How to use fp?
To use fp, you must include the fp.js or fp.min.js first.  
A simple example:
```html
<script type="text/javascript" src="./fp.min.js"></script>
<script type="text/javascript">
  fp(function(myFp){
      alert(myFp);
  });
</script>
```

## Advanced Usage

### Get fp
```html
<script type="text/javascript" src="./fp.min.js"></script>
<script type="text/javascript">
  fp(function(myFp, key, acc, detail, createdTime, timeUsed, detailObj){
      console.log('My fp: ' + myFp);
      console.log('fp key: ' + key);
      console.log('Accuracy: ' + acc);
      console.log('fp Details: ' + detail);
      console.log('fp Created Time: ' + createdTime);
      console.log('Time Usage to calculate: ' + timeUsed);
      console.log(detailObj);
  });
</script>
```

### Recover fp from key (cross-domain purpose)
```html
<script type="text/javascript" src="./fp.min.js"></script>
<script type="text/javascript">
  fp(/*fp key*/'eyJfZnAiOiI1YjI4Y2U5ZCIsIl9mcF9yZWZfIjoiZVZiSmJVVjlWNGFzS0JZOE10THRZQmJVTkVkSkk5WUpJZElnYlJJUVpWY0lhZGJKZVFZNWI5TkVMRmJKWlZJZ09KZTlkMEwxWkZVZExOVUZJVWJOWkpJNVpvWkZhOVpVY0ZjSklCY0pZeEl4Y0pNQmJKYlJkeFlCYkJZQlk0YlViQlpoSUJaRllGWUZiY0xaY1JZQllRVHRRTlpsUmxkSlFkSUZiOVlZUUJRNVZGUUZRaFRWV0ZlTmRJWVZRVlpKYjVUQVprUmhOUmRFTkJNSmJvWmhaNVpKWmhaTmFvY0phTWN3VEpaSlpSVTlJWkxOWk1jeGJGY0JiRmExTEpUeFk1TE5MSlFsSVZPUU5ZTyIsIl9mcF9MYXN0Q2hhbmdlVGltZSI6IjE1NjE1MTkxNzYifQ==',
      function(myFp, key, acc, detail, createdTime, timeUsed, detailObj){
          console.log('My fp: ' + myFp);
          console.log('fp key: ' + key);
          console.log('Accuracy: ' + acc);
          console.log('fp Details: ' + detail);
          console.log('fp Created Time: ' + createdTime);
          console.log('Time Usage to calculate: ' + timeUsed);
          console.log(detailObj);
      });
</script>
```

### Reset fp
```html
<script type="text/javascript" src="./fp.min.js"></script>
<script type="text/javascript">
  fp('reset', function(myFp, key, acc, detail, createdTime, timeUsed, detailObj){
      console.log('My fp: ' + myFp);
      console.log('fp key: ' + key);
      console.log('Accuracy: ' + acc);
      console.log('fp Details: ' + detail);
      console.log('fp Created Time: ' + createdTime);
      console.log('Time Usage to calculate: ' + timeUsed);
      console.log(detailObj);
  });
</script>
```

### Cookie
fp preloads [iotcat/cookie-js](https://github.com/iotcat/cookie-js), support all of its functions.    

**usage**    
`cookie.set(key, val, days)`: set a cookie, with key name, value, days to live(defaule: 10 years)   
`cookie.get(key)`: get cookie with key    
`cookie.del(key)`: delete cookie with key    

**example**
```js
//set a cookie named iotcat，its value is hero，live for 30 days
cookie.set("iotcat", "hero", 30);

//get the value of the cookie iotcat
alert(cookie.get("iotcat"));

//delete the cookie of iotcat
cookie.del("iotcat");
```

## CDN
 - China: `https://cdn.yimian.xyz/fp/fp.min.js`

## Background
This project is developed from https://github.com/Valve/fingerprintjs2   



## License
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FIoTcat%2Ffp.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2FIoTcat%2Ffp?ref=badge_large)