# go-casbin-acl-filebased-example
An example of how to use casbin as an ACL service with file-based configuration

# Setup
## Install dependencies
```
$ go install github.com/casbin/casbin/v2@latest
$ go get github.com/casbin/casbin/v2
```

## Compiling
```
$ go build server/main.go
```

## Running
```
$ go run server/main.go <user> <resource> <action>
```

# Configuration
The ACL policy is provided in `policy.csv`
```
p, alice, data1, read
p, bob, data2, write
```

The definition of each line within the file defines that:
1. `alice` has `read` access to `data`
2. `bob` has `write` access to `data2
