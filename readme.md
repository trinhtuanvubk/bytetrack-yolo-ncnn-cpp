# Install NCNN

<!-- https://waittim.github.io/2020/11/10/build-ncnn/ -->
- To install ncnn with gpu (ubuntu):
```
wget https://sdk.lunarg.com/sdk/download/1.2.154.0/linux/vulkansdk-linux-x86_64-1.2.154.0.tar.gz?Human=true -O vulkansdk-linux-x86_64-1.2.154.0.tar.gz
tar -xf vulkansdk-linux-x86_64-1.2.154.0.tar.gz
export VULKAN_SDK=$(pwd)/1.2.154.0/x86_64
```

- To install ncnn with cpu (ubuntu):
```bash
git clone https://github.com/Tencent/ncnn.git
cd ncnn
mkdir -p build
cd build
cmake -DCMAKE_BUILD_TYPE=Release -DNCNN_VULKAN=OFF -DNCNN_SYSTEM_GLSLANG=ON -DNCNN_BUILD_EXAMPLES=ON ..
make
make install
```

