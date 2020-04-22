# golang useful cmds
```
go vet ../...
goimports -w ../
go fmt ../...
golint ../...

go test ../...    # test all test.go under this folder
```


# golang test cover
```
# output coverfile
go tool -coverprofile=cover.out -o coverage.html

# html viewer for cover.out, and will output in /tmp
go tool cover -html=cover.out 

# get not covered func
grep -r -B15 --color=auto cov0 coverage.html |grep func 
```

# how to remove go's plugin 
```
go clean -i -n github.com/nsf/gocode
# 以下の内容が表示されるので、削除内容を確認します。
  cd $GOPATH/src/github.com/nsf/gocode
  rm -f gocode gocode.exe...(略)
go clean -i github.com/nsf/gocode
# src以下に残っているものを削除します
ls $GOPATH/src/github.com/nsf
rm -rf $GOPATH/src/github.com/nsf 
```

# ctags for golang
- [gotags - github](https://github.com/jstemmer/gotags)	
   
# gdb for golang
```
go build -gcflags "-N -l" gdbfile.go
gdb gdbfile
```
