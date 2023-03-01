# compile-gRPC-windows

```
md .build
cd .build
cmake .. -DgRPC_BUILD_TESTS=OFF -DCMAKE_INSTALL_PREFIX=E:\network\grpc_install
cmake --build . --config Release
cmake --install ../.build
```
