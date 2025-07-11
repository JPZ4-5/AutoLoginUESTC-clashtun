# UESTC 电子科技大学网络认证脚本
------------------------------
把查询从ping改成curl。

clash的tun模式会劫持ping，导致无法正确判断是否连上校园网。

叉的https://github.com/b71db892/AutoLoginUESTC

---

- 校园网有线接入+学号认证（在主楼做的测试，至今可用）
- 移动、电信寝室宽带有线接入+学号认证（类似于硕丰6、7、8组团那种插网线直接弹出认证页面的，至今可用）
- 在信通楼，认证页面为10.253.0.237
- *信通楼也有可能是10.253.0.235*，输入时若不对会自动跳转。
  
只需修改config.py就行。然后手动注销断网，输入：
```angular2html
python login_once.py
```
如果能联网，那说明配置没问题。

之后一直运行always_online.py就行了。
```angular2html
python always_online.py  
```

可以使用自动任务计划挂在后台，例如把pythonw always_online.py作为bat挂在开机运行里。
