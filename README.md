# timeout

This is a python package for taking some bunch of codes under timeout check. This breaks a block of code or a function when a timeout limit is reached.

This package can be used both as decorator for a function or as context for a bunch of codes.

## Example:
### As a decorator:
```
@timeout(timeout=10, message='Your script timed out')
    def funct():
        while True:
            print 'Hello world!'
```

### As context:
```
with timeout(timeout=10, message='Your loop timedout'):
        while True:
            print 'Hello world!'
```

### Parameters:
`timeout`: Parameter to define your timeout in seconds. By default, this parameter is set to 10
`message`: Your manual message to show with the TimeoutError exception. By default, this parameter is set as 'Timed out'
