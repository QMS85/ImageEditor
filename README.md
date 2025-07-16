# 🖼️ Image Editor App (Python + Tkinter)  

A simple, user-friendly image editor built with Python, Tkinter, and Pillow (PIL). This app allows you to load, display, apply filters, reset, and save images with a clean graphical interface.  

---  

## ✨ Features  

- **Load Images:** Supports JPG, PNG, BMP, GIF, and more.  
- **Display Images:** Automatically resizes images for display.  
- **Apply Filters:** Blur, Contour, Edge Enhance, Emboss, Sharpen, Smooth.  
- **Reset:** Revert to the original image at any time.  
- **Save:** Export your edited image in PNG or JPEG format.  
- **Simple GUI:** Intuitive interface using Tkinter.  

---  

## 🛠️ Installation  

### 1. Clone the Repository  

```bash  
git clone https://github.com/yourusername/ImageEditor.git  
cd ImageEditor  
```  

### 2. Create a Virtual Environment (Recommended)  

```bash  
python3 -m venv venv  
source venv/bin/activate  
```  

### 3. Install Required Libraries  

```bash  
pip install pillow  
```  

> **Note:** Tkinter is included with most Python installations. If not, install it via your package manager:  
> - **Ubuntu/Debian:** `sudo apt-get install python3-tk`  
> - **Fedora:** `sudo dnf install python3-tkinter`  
> - **Windows/Mac:** Usually included with Python.  

---  

## 🚀 Running the App  

```bash  
python app.py  
```  

The GUI window will open. Use the buttons to load, edit, and save images.  

---  

## 🧩 Project Structure  

```
ImageEditor/  
├── app.py         # Main application code  
├── README.md      # Project documentation  
└── ...            # (Add your images or other files here)  
```  

---  

## 🖥️ Deployment Options  

### 1. **Run Locally**  
- Follow the installation steps above.  

### 2. **Create a Standalone Executable**  
- Use [PyInstaller](https://pyinstaller.org/) to bundle the app for Windows, macOS, or Linux:  

```bash  
pip install pyinstaller  
pyinstaller --onefile --windowed app.py  
```  
- The executable will be in the `dist/` folder.  

### 3. **Docker Deployment**  
- Create a `Dockerfile`:  

    ```dockerfile  
    FROM python:3.11-slim  
    RUN apt-get update && apt-get install -y python3-tk  
    WORKDIR /app  
    COPY . /app  
    RUN pip install pillow  
    CMD ["python", "app.py"]  
    ```  

- Build and run:  

    ```bash  
    docker build -t image-editor .  
    docker run -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix image-editor  
    ```  

    > **Note:** For GUI apps in Docker, you need to allow X11 forwarding.  

---  

## 📦 Requirements  

- Python 3.7+  
- Pillow (PIL)  
- Tkinter (GUI library, usually included with Python)  

---  

## 📚 References  

- [Pillow Documentation](https://pillow.readthedocs.io/en/stable/)  
- [Tkinter Documentation](https://docs.python.org/3/library/tkinter.html)  
- [Original Tutorial](https://hackr.io/blog/how-to-create-a-python-image-editor-app)  

---  

## 📝 License  

This project is open-source and free to use under the [MIT License](LICENSE).  

---  

## 🙋‍♂️ Contributing  

Pull requests and suggestions are welcome! Please open an issue to discuss changes.  

---
