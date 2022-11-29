# PyQt-DataAcquisition

## Installation

To install:
```
pip install opencv-python
pip install more_itertools
pip install selenium
pip install pool
pip install pyqt5
pip install pyqt5-tools
```
- Configuring the Browser Driver (Google Chrome)
* [Find the version number of your Google browser and download the corresponding browser driver](https://registry.npmmirror.com/binary.html?path=chromedriver/)


## Getting Started

It takes only several lines of code to create a simple demo.

```python
import sys
from PyQt5 import uic
from PyQt5.QtWidgets import QApplication, QWidget

class MyWidget(QWidget):

    def __init__(self, parent=None):
        super(MyWidget, self).__init__()
        self.ui = uic.loadUi("./MyUI.ui")

if __name__ == '__main__':

    myapp = QApplication(sys.argv)
    myWidget = MyWidget()
    myWidget.ui.show()
    sys.exit(myapp.exec_())
```

Before running this code you need to design a UI file, MyUI.ui

First, you need to configure External Tools:

Click on PyCharm's File->Settings->Tools0->External tools, Open the window for adding external tools. Press '+' to enter the window for adding external tools. 

![image](https://user-images.githubusercontent.com/95462696/204622394-afb58711-75dc-4934-8fe1-a8c8d7134f15.png)

Enter a tool Name at 'Name'.Then, locate the directory where you installed designer.exe (usually in the Lib\site-packages\pyqt5_tools folder in your python installation directory) and copy the directory to 'Programs', taking care to include the name of the designer.exe file. Set your own Working path in the Working directory. The ui file generated by qtdesigner will be saved in this path by default. Don't set 'Arguments', just confirm.

![image](https://user-images.githubusercontent.com/95462696/204622257-8e8e9f0f-47d4-4f6c-8ed5-30e7ac4175e1.png)

Now you can check whether the configuration is successful

![image](https://user-images.githubusercontent.com/95462696/204622731-32600f77-9007-465a-9707-950e79110c9b.png)

Run Qt Designer, design an interface and save it as 'MyUI.ui'

![image](https://user-images.githubusercontent.com/95462696/204623230-b9b6ebc5-f7e1-49f2-858f-63f545e56abb.png)

Now you can run that code and get the simplest GUI program you can

![image](https://user-images.githubusercontent.com/95462696/204623713-ca7ebc21-f602-44f5-8a06-e768cc218406.png)

## Key Features

- With perfect functions
  * download pictures from the website
  * take photos and record videos from the camera
  * import videos for screenshots

- Simple and comfortable UI design
  * By graphical buttons
  * By optimizing the code

- The home screen won't get stuck
  * The child thread executes the time-consuming task, overriding the run() method
  * Custom signal passing return value

- The 'Internet module' can get dynamic front-end code instead of just static front-end code
  * Selenium can parse dynamic web information generated by JavaScript files

- You can get the original image instead of the thumbnail
  * Get the url of the detailed page first, and then find the original image to get the url of the original image



