## protobuf
    1. 在如下网址(https://github.com/protocolbuffers/protobuf/releases)下载对应版本的二进制文件，解压
    2. 拷贝到可执行目录 cp * /usr/local/ -R
    3. go get github.com/golang/protobuf/protoc-gen-go
    4. go get github.com/golang/protobuf/proto
    5. 编写 $project_path/pb/test.proto
    6. 生成文件 cd $project_path/pb/ && protoc --go_out=. test.proto
    7. 编写$project_path/main.go
    8. go run $project_path/main.go

## grpc 安装
    git clone https://github.com/grpc/grpc-go.git $GOPATH/src/google.golang.org/grpc

    git clone https://github.com/golang/net.git $GOPATH/src/golang.org/x/net

    git clone https://github.com/golang/text.git $GOPATH/src/golang.org/x/text

    go get -u github.com/golang/protobuf/{proto,protoc-gen-go}

    git clone https://github.com/google/go-genproto.git $GOPATH/src/google.golang.org/

    cd $GOPATH/src/

    go install google.golang.org/grpc
    
    protoc --go_out=plugins=grpc:. test.proto
    