# git-log-weekly-report

[使用git log命令自动生成周报](https://blog.yeatse.com/2016/03/07/git-log-weekly-report)

Generate weekly report and save it to a specified file. Modified from [pkyeck/git-log-by-day](https://github.com/pkyeck/git-log-by-day).

# Usage:

```bash
curl -O "https://raw.githubusercontent.com/yeatse/git-log-weekly-report/master/git-weekly-report.sh"
chmod +x git-weekly-report.sh
./git-weekly-report.sh -r <path-to-your-repository>  # log file will be saved to yyyy-MM-dd.log.

# Or a little more complicated:
./git-weekly-report.sh -s last.Month -e yesterday -a someone -o logfile.log  # git log between last month and yesterday will be output.
```

# Sample output:

```
[2016-02-29]
* Update elctron-prebuilt version. Fix #11.
* Optimize user's avatar display in Linux.
* Disable zooming in the app.

[2016-03-01]
* Introduce travis CI.
* Fix tar-all chmod.
* Introduce gitter.
* Update docs for the new release.
* Fix travis deployment files.
* Fix wrong regex which might cause stickers not showing in group chat.
* Force travis work.
* Update travis config and wrong regex.

[2016-03-04]
* Remove unnecessary dev tools.
* Take control of quit event. Press Cmd+Q to quit, and Cmd+W to hide window.

[2016-03-05]
* Modify implementation of listening message change, which caused scrolling jank. Fix #66.
* Revert <q>修正消息统计</q>
* Take control over reload. Useful when session timeout and needs refresh.
* Improve experience on the Linux platform. Specifically fix wrong app icon, add tray icon, add menu and override shortcuts.
```
