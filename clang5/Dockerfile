FROM ubuntu:16.04

RUN apt-get update && apt-get install -y \
    xz-utils \
    build-essential \
    curl \
    && rm -rf /var/lib/apt/lists/*

RUN curl -SL http://releases.llvm.org/5.0.0/clang+llvm-5.0.0-linux-x86_64-ubuntu16.04.tar.xz \
    | tar -xJC . && \
    mv clang+llvm-5.0.0-linux-x86_64-ubuntu16.04 clang_5.0.0 && \
    echo 'export PATH=/clang_5.0.0/bin:$PATH' >> ~/.bashrc && \
    echo 'export LD_LIBRARY_PATH=/clang_5.0.0/lib:LD_LIBRARY_PATH' >> ~/.bashrc
