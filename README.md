### feature
strings obfucation by alloca const c strings on stack. 
### build:
#### 1.
clone this repo 
#### 2.
replace some files in `${llvm_17.0.3_src/llvm/lib/Passes/}` with corresponding files in the repo. 

#### 3.
build with command:
cmake -DLLVM_ENABLE_PROJECTS="clang;lld;" -DCMAKE_C_FLAGS=/utf-8 -DCMAKE_CXX_FLAGS=/utf-8 -DLLVM_INCLUDE_DOCS=OFF -DLLVM_INCLUDE_TESTS=OFF -DLLVM_INCLUDE_EXAMPLES=OFF -DLLVM_INCLUDE_BENCHMARKS=OFF  -DLLVM_TARGETS_TO_BUILD="X86" -G "Visual Studio 17 2022" -A x64 -Thost=x64 ..\llvm
