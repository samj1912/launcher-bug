Reproduction -


`pack build --buildpack start test`

```
$ docker run test '{"test": "test"}'
{test: test}
```

`docker build . --tag test`

```
$ docker run test '{"test": "test"}'
{"test": "test"}
```

