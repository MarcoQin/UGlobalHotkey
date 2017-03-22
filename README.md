## UGlobalHotkey

### Decription  
UGlobalHotkey is an extension for Qt framework, which implements global hotkeys functionality for Windows Linux and MacOSX platforms.
It is written by [bakwc](https://github.com/bakwc), extracted from [Pastexen](https://github.com/bakwc/Pastexen) and turned into a shared library by me.

### Building from source  
* You can either open project with QtCreator and press Build button
* Or build it using terminal:
``` 
qmake  
make
```
* This will build shared library in source directory, like libUGlobalHotkey.dylib or something else.

### Usage example  
``` 
UGlobalHotkeys *hotkeyManager = new UGlobalHotkeys(); 
hotkeyManager->registerHotkey("Ctrl+Shift+F12");
connect(hotkeyManager, &UGlobalHotkeys::activated, [=](size_t id)
{
    qDebug() << "Activated: " << QString::number(id);
});
```
You need add something to your xxx.pro file, for example:
```
LIBS += -L/Path/To/UGlobalHotkey -lUGlobalHotkey
INCLUDEPATH += /Path/To/UGlobalHotkey
```
Then you can use this library now:
```
#include "uglobalhotkeys.h"
```

### License  
UGlobalHotkey library is licensed as Public Domain, so you are free to do anything with it.
