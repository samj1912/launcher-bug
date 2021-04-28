Reproduction -


`pack build --buildpack start test`

```
$ docker run test '{"test": "test"}'
{test: test}
```

After changing direct=false to direct=true it works as expected - 


`pack build --buildpack start test`

```
$ docker run test '{"test": "test"}'
{test: test}
```

but I lose the ability to have profile.d scripts which I want.

`docker build . --tag test`

```
$ docker run test '{"test": "test"}'
{"test": "test"}
```

