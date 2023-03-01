# compile-build-gRPC-windows

- https://github.com/grpc/grpc/blob/master/BUILDING.md
- https://grpc.io/docs/languages/cpp/quickstart


## Build gRPC
```
git clone --recursive https://github.com/gmh5225/grpc
md .build
cd .build
cmake .. -DgRPC_BUILD_TESTS=OFF -DCMAKE_INSTALL_PREFIX=E:\network\grpc_install
cmake --build . --config Release
cmake --install ../.build
```

## Build the example
```
git clone --recursive https://github.com/gmh5225/grpc
cd examples/cpp/helloworld
md .build
cd .build
cmake -DCMAKE_PREFIX_PATH=E:\network\grpc_install ../
cmake --build . --config Release
```
