## 目录

- [字体](#字体)
- [QPushButton](#QPushButton)
- [QDockWidget](#QDockWidget)
- [QTableView](#QTableView)
- [](#)
- [](#)
- [](#)
- [其它链接](#其它链接)

## 字体

```c++
// 设置全局字体
QFont font;
font.setFamily("MS Shell Dlg 2");
qApp->setFont(font);

// 输出当前系统下的所有字体
QFontDatabase database;
foreach (const QString &family, database.families())
{
    qDebug() << family;
}

// 检测全局字体
qDebug() << qApp->font().rawName();
qDebug() << qApp->font().family();
qDebug() << qApp->font().defaultFamily();
qDebug() << qApp->font().styleName();
qDebug() << qApp->font().toString();
qDebug() << qApp->font().key();
```

## QPushButton

```css
QPushButton {
    color: white;
    background-color: #17a2b8;
    border-color: #17a2b8;
    border: 1px solid transparent;
    padding: 6px 12px;
    font-size: 16px;
    line-height: 1.5;
    border-radius: 4px;
}
```

参考：

- <https://blog.csdn.net/wanyongtai/article/details/80189299>
- <https://github.com/danielepantaleone/eddy/blob/master/resources/styles/QPushButton.qss>
- <https://www.cnblogs.com/linuxAndMcu/p/11039814.html>

## QDockWidget

参考：

- <https://github.com/danielepantaleone/eddy>
- <https://blog.csdn.net/wzs250969969/article/details/78466143>

## QTableView

参考：

- <https://github.com/lowbees/Hover-entire-row-of-QTableView>

## 其它链接

- [Bootstrap](https://www.runoob.com/bootstrap4/bootstrap4-tutorial.html)
- [Qt Style Sheets Examples](https://doc.qt.io/qt-5/stylesheet-examples.html)
- [https://github.com/satchelwu/QSS-Skin-Builder](https://github.com/satchelwu/QSS-Skin-Builder)
- [https://github.com/chenwen1126/Qss](https://github.com/chenwen1126/Qss)
