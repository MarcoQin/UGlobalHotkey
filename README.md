## UGlobalHotkey

### Decription  
UGlobalHotkey is an extension for Qt framework, which implements global hotkeys functionality for Windows and Linux platforms.
It is written by [bakwc](https://github.com/bakwc) and extracted from [Pastexen](https://github.com/bakwc/Pastexen) and turned into shared library by me.

### Building from source  
* You can either open project with QtCreator and press Build button
* Or build it using terminal:
``` 
qmake
make
```

### Usage example  
``` 
UGlobalHotkeys *hotkeyManager = new UGlobalHotkeys(); 
hotkeyManager->RegisterHotkey("Ctrl+Shift+F12");
connect(hotkeyManager, &UGlobalHotkeys::Activated, [=](size_t id)
{
    qDebug() << "Activated: " << QString::number(id);
});
```