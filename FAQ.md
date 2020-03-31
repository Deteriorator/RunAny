## 1. 无法获取QQ聊天内容问题解决

使用<kbd>Win</kbd>+<kbd>字母</kbd>热键无法取得QQ聊天窗口内容

**原因**：因为QQ聊天窗口是绘制的特殊窗体，不是Windows系统常见控件，所以目前无法用AHK的<kbd>Win</kbd>+热键去获取其内容

**解决**：换一个其他的比如<kbd>Alt</kbd>+<kbd>字母</kbd>、<kbd>Ctrl</kbd>+<kbd>字母</kbd>、<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>字母</kbd>之类就正常了

---

## 2. RunAny菜单无法消失问题解决

#### Win10 1709版本使用<kbd>Win</kbd>+<kbd>`</kbd>热键显示RunAny菜单后，菜单不消失

**原因**：因为1709系统对<kbd>Win</kbd>+热键的控制，导致出现菜单后需要点一下菜单中的内容才会关闭菜单

**解决**：不升级系统的情况下，更换RunAny的热键，不带有Win键

#### 极少情况下在Win10中安装360安全卫士导致RunAny菜单无法消失

**原因**：目前尚未清楚是360安全卫士哪项设置导致，欢迎告知

**解决**：卸载360安全卫士后菜单恢复正常

---



## 3. 在Total Command，Directory Opus中RunAny没有获取到选中文件

**原因**：因某些不明配置原因，导致在TC、DO中按<kbd>Ctrl</kbd>+<kbd>C</kbd>复制文件速度变慢，没在短时间给RunAny文件信息误判断为无选中文件

**解决**：手动修改RunAny配置`RunAnyConfig.ini`，使用隐藏配置延长等待复制时间：

```ini
[Config]
ClipWaitApp=TotalCMD64.exe
ClipWaitTime=2
```

> 在[Config]下添加 <br>
> ClipWaitApp（在什么应用界面延长等待复制时间, 多个逗号分隔） <br>
> ClipWaitTime（最长等待复制的时间（2秒）大概在1.5秒以上可以稳定获取到）



---
