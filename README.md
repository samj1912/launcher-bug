Reproduction -


`pack build --buildpack start test`

This doesn't work as it strips the double quotes
```
$ docker run test '{"test": "test"}'
{test: test}
```

This works 
```
$ docker run test "{\"test\": \"test\"}"
{"test": "test"}
```


After changing direct=false to direct=true it works as expected - 


`pack build --buildpack start test`
This works as expected
```
$ docker run test '{"test": "test"}'
{"test": "test"}
```
This also works
```
$ docker run test "{\"test\": \"test\"}"
{"test": "test"}
```

but I lose the ability to have profile.d scripts which I want.

Finally with a pure docker build - 

`docker build . --tag test`

```
$ docker run test '{"test": "test"}'
{"test": "test"}
```

