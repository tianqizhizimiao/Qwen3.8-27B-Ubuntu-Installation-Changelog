## 安装llama
### 拉取源码
```bash
git clone --depth=1 https://github.com/ggml-org/llama.cpp.git
```

### 安装编译工具
```bash
apt update
apt install build-essential cmake
```

### 编译
```bash
# 创建 build 构建目录
mkdir build
cd build

# 生成构建文件
cmake ..

# 编译
cmake --build . -j$(nproc)
```

### 注册入环境变量(可选)
```bash
echo 'export PATH="/youPath/build/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```
- 或则直接进入 /youPath/build/bin

### 进行测试
```bash
llama-server --help
```
- 若无报错即成功
