# NT120 — Lecture 03 code notes

Notebook học Python, NumPy và Pandas, được tách từ slide Lecture 03.

```text
slides/               PDF bài giảng
notebook/chapter03/   Bốn notebook theo chủ đề và notebook tổng `lecture_03.ipynb`
data/                 Dữ liệu CSV mô phỏng
```

## Cài Miniconda

### Linux (x86-64)

```bash
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh
```

Khi installer hỏi khởi tạo Conda cho shell, chọn `yes`, sau đó đóng/mở lại Terminal.

### Windows (PowerShell)

```powershell
Invoke-WebRequest -Uri "https://repo.anaconda.com/miniconda/Miniconda3-latest-Windows-x86_64.exe" -OutFile "$env:USERPROFILE\Downloads\Miniconda3-latest-Windows-x86_64.exe"
Start-Process "$env:USERPROFILE\Downloads\Miniconda3-latest-Windows-x86_64.exe" -Wait
```

Sau khi installer hoàn tất, mở **Anaconda Prompt (Miniconda3)** để chạy các lệnh bên dưới.

## Tạo môi trường và chạy trong VS Code

```bash
conda tos accept --override-channels --channel https://repo.anaconda.com/pkgs/main
conda tos accept --override-channels --channel https://repo.anaconda.com/pkgs/r
conda create -n nt120 python=3.10 -y
conda activate nt120
python -m pip install -r requirements.txt
python -m ipykernel install --user --name nt120 --display-name "nt120 (Python 3.10)"
```

Mở notebook trong VS Code, chọn kernel **nt120 (Python 3.10)**, rồi chạy theo thứ tự:

1. `notebook/chapter03/01_colab_setup.ipynb` — Colab và setup
2. `notebook/chapter03/02_python_numpy.ipynb` — Python cơ bản và NumPy
3. `notebook/chapter03/03_pandas_exploration.ipynb` — đọc, kiểm tra và khám phá dữ liệu
4. `notebook/chapter03/04_pandas_cleaning_reproducibility.ipynb` — làm sạch và tái lập kết quả

Notebook 3 và 4 tự tạo `data/flows.csv` mẫu khi chạy.

Nếu muốn học trong một file duy nhất, mở `notebook/chapter03/lecture_03.ipynb`.
