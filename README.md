# Video edge detection

Use opencv-python library to detect the edge of anime video.

## Environment
- Python 3.7+

## Setup
install dependencies:

pip install tqdm==4.64.0 matplotlib==3.4.3 moviepy==1.0.3 numba==0.56.2 numpy==1.21.6 opencv-python==4.5.4.60 pygame


## Usage

edit `canny.py` options as follows:

# 高斯模糊的核大小，必须为 (3,3) 或 (5,5) 或(7,7)
gaussian_ksize = (3, 3)
# 输出视频的背景颜色，RGB 格式，必须为数组格式
bg_color_rgb = [237, 244, 247]
# 输出视频的线条颜色，RGB 格式，必须为数组格式
line_color_rgb = [173, 155, 236]
# canny 低阈值
canny_low_threshold = 30
# canny 高阈值，一般为低阈值的 2 或 3 倍
canny_high_threshold = 90
# 形态学膨胀核，修复 canny 边缘检测后的线条太细的问题, 核越大，线条越粗。
dilation_ksize = (2, 2)
# 输入视频的路径
input_video_path = "materials/videos/2007-autumn-anime-spot-op.mp4"
# 输出视频的文件夹，手动创建保证存在
output_folder = "output"

## Then run command:bash

sudo python canny.py
