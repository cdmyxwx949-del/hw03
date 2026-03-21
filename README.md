# hw03
人脸检测/识别

先确认你的 Python 版本和系统方法
在 Jupyter 里用 Python 代码查看
在单元格里输入并运行：
import sys
print(sys.version)

我的Python 版本是 3.11.7（64 位，Anaconda 环境），若运行出现问题，直接问ai，非常便捷。

1. 下载匹配版本的 .whl
文件需要下载文件名包含 cp311 和 win_amd64 的 triton 包
2. 执行安装命令
把下载好的文件放到桌面，在 PowerShell 中执行：
cd C:\Users\Desktop
pip install triton-2.0.0-cp311-cp311-win_amd64.whl

环境配置：# 1. 安装核心依赖（管理员身份打开 PowerShell）
pip install face_recognition streamlit pillow numpy opencv-python -i https://pypi.tuna.tsinghua.edu.cn/simple

# 2. 切换到代码所在目录（如桌面）
cd C:\Users\32414\Desktop

# 3. 启动应用
streamlit run face_recognition_app.py

系统依赖环境：
# 1. 安装核心依赖（管理员身份打开 PowerShell）
pip install face_recognition streamlit pillow numpy opencv-python -i https://pypi.tuna.tsinghua.edu.cn/simple

# 2. 切换到代码所在目录（如桌面）
cd C:\Users\Desktop

# 3. 启动应用
streamlit run app.py

操作流程：
运行命令后，自动打开浏览器（地址：http://localhost:8501）；
侧边栏查看实验说明，主界面点击「上传图片」选择人脸照片；
点击「开始检测」按钮，等待几秒后查看：
标注人脸位置的图片；
每个人脸的坐标 + 128 维特征向量；
特征值分布图表。

满足以下条件的图片可以被正常识别：
1. 格式要求
支持格式：JPG（.jpg/.jpeg）、PNG（推荐优先用 JPG）
不支持格式：GIF 动图、WebP、BMP、带透明通道的特殊 PNG、16 位深度专业摄影图
位深度：必须是 8 位灰度图或 8 位 RGB 彩色图（dlib 只认这两种）
