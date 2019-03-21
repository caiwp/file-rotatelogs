file-rotatelogs
==================

Add MaxSize option and remove rotating files forcefully based on [github.com/lestrrat-go/file-rotatelogs](https://github.com/lestrrat-go/file-rotatelogs)

OPTIONS
====

## MaxSize

If the value of MaxSize is set, it will be rotated according to whether 
the file content size exceeds this value.

```go
  rotatelogs.New(
    "/var/log/myapp/log.%Y%m%d",
    rotatelogs.WithMaxSize(10*1024*1024), // 10M
  )
```

And you will get a log file name in like `2018.log.1`, `2018.log.2`, etc.
