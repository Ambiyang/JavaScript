```
electron-packager
npm install electron-packager -g
```

1. show window graceful
```
win = new BrowserWindow({show:false});
win.loadFile('index.html');
win.on('ready-to-show',()=>{
  win.show()
})
```

2. parent windows
```
parentWin = new BrowserWindow();
childWin = new BrowserWindow({parent:parentWin});

parentWin.loadFile('index1.html');
parentWin.loadFile('index2.html');
```

3. motai windows
```
parentWin = new BrowserWindow();
childWin = new BrowserWindow({parent:parentWin,width:200,height:200,modal:true});

parentWin.loadFile('index1.html');
parentWin.loadFile('index2.html');
```

4. close multiple windows
```
parentWin = new BrowserWindow();
childWin = new BrowserWindow({parent:parentWin,width:200,height:200,modal:true});

parentWin.loadFile('index1.html');
parentWin.loadFile('index2.html');
```

5. child window also receive ipcMain.on
```
use file name to filter
if (__dirname + '\\index.html' == __filename) {
		get_confirm_window(obj);
	}
```

6. how to check undefined
```
if (typeof(win_confirm) == 'undefined')
```




