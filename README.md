## 1.
clone this repo 
replace some files in `${llvm_17.0.3_src/llvm/lib/Passes/}` with corresponding files in the repo. 
build command:
cmake -DLLVM_ENABLE_PROJECTS="clang;lld;" -DCMAKE_C_FLAGS=/utf-8 -DCMAKE_CXX_FLAGS=/utf-8 -DLLVM_INCLUDE_DOCS=OFF -DLLVM_INCLUDE_TESTS=OFF -DLLVM_INCLUDE_EXAMPLES=OFF -DLLVM_INCLUDE_BENCHMARKS=OFF  -DLLVM_TARGETS_TO_BUILD="X86" -G "Visual Studio 17 2022" -A x64 -Thost=x64 ..\llvm
