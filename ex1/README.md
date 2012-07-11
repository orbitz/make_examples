This is an example of a Makefile that implements walking subdirectories.  The idea is to
have one list of subdirectories and to automatically build make all, make test, and make clean
without writing all of the dependencies each time.

Expected output:

    orbitz@52:~/projects/make_examples/ex1(master)$ make
    make -C s1
    echo "all"
    all
    make -C s2
    echo "all"
    all
    make -C s3
    echo "all"
    all
    orbitz@52:~/projects/make_examples/ex1(master)$ make test
    make -C s1 test
    echo "all"
    all
    echo "test"
    test
    make -C s2 test
    echo "all"
    all
    echo "test"
    test
    make -C s3 test
    echo "all"
    all
    echo "test"
    test
    