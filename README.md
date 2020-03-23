# vsiaie
Distribution repository for VSI auto vectorization 

cd ./llvm-project/vsi-aeibe/test/vectorize_tests
edit ./clang_cmd.sh
replace ~/llvm-exec with the directory you untarred into
three testcases.
        test1.cc, keysight_test.cc, do_sine.cc, do_cos.cc
to vectorize into AIE kernel

./clang_cmd -O test1 test_func { -O optimization, test1 Source file name , test_func top-level function }
output will be test1.cpp {Source filename.cpp}

Note: it is important to have __restrict__ for inputput and output parameters.
