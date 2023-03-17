# compile-build-gRPC-windows

- https://github.com/grpc/grpc/blob/master/BUILDING.md
- https://grpc.io/docs/languages/cpp/quickstart


## Build gRPC
```
git clone --recursive https://github.com/gmh5225/grpc
md .build
cd .build

cmake .. -DgRPC_BUILD_TESTS=OFF -DCMAKE_INSTALL_PREFIX=E:\network\grpc_install 
or
cmake .. -DgRPC_BUILD_TESTS=OFF -DCMAKE_INSTALL_PREFIX=E:\network\grpc_install_llvm -TLLVM-MSVC_v143

cmake --build . --config Release
cmake --install ../.build
```

## Build the example from grpc
```
git clone --recursive https://github.com/gmh5225/grpc
cd examples/cpp/helloworld
md .build
cd .build

cmake -DCMAKE_PREFIX_PATH=E:\network\grpc_install ../
or
cmake -DCMAKE_PREFIX_PATH=E:\network\grpc_install_llvm ../

cmake --build . --config Release
```

## Build the example from this repo
- Download [compiled gprc binary](https://github.com/gmh5225/compile-build-gRPC-windows/releases/tag/gmh-740932c899a3a978f75bfa8092e7b02f1740bf62)
- Put it into E:\network\grpc_install
- Run build-win-64.bat
