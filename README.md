# C++ CMake template with unit testing capabilities

## Geting started

1. Configure your project in top-level [`CMakeLists.txt`](CMakeLists.txt).
2. Add third-party dependencies in [`contrib/CMakeLists.txt`](contrib/CMakeLists.txt).
3. Write your awesome code in [`src`](src) and [`include`](include) folders by creating header and source files.
4. Configure and create top notch unit tests in [`tests`](tests) folder using `Catch2` and `FakeIt` frameworks.
5. Develop you project without any worry using provided CI workflows (with memory leaking check).

## Q&A

> Where can I see CI workflow status?

Well, click on `Actions` button and you will see "Check memory leaks workflow" section.

This workflow runs on demand, i.e. manual launch is required. 

>  How to clone and build this project?

```shell
git clone --recurse-submodules -j2 <repository url>
```

and from the project's folder:
```shell
mkdir -p build && cd build

cmake -DCMAKE_BUILD_TYPE=Release ..
cmake --build . --config Release
```

> What about running tests?

Build the project and run the following:

```shell
ctest -VVV
```
