# 工时记录 APP

一个简洁的工时记录与收入计算应用。

## 功能特点

- 📅 日历视图记录每日工时
- 💰 两种计薪方式：
  - **底薪+加班费**（平时1.5倍，周末2倍，法定假日3倍）
  - **按时薪**
- 🔄 自定义计薪周期（如1号~30号、15号~14号等）
- 📊 年总工时和收入统计
- ⚙️ 所有参数可随时修改

## 在手机上构建APK

### 方法一：通过 GitHub Actions（推荐）

1. 在 GitHub 上创建新仓库
2. 将本项目所有文件上传到仓库
3. 进入仓库 → Actions 标签页
4. 点击 "Build APK" → "Run workflow"
5. 等待构建完成，下载生成的 APK 文件

### 方法二：通过 AIDE（Android IDE）

1. 在手机上安装 [AIDE](https://aide.app/)
2. 将项目导入 AIDE
3. 点击运行 → 直接生成 APK

### 方法三：通过 Termux

```bash
pkg install openjdk-17
# 下载 Android SDK 命令行工具
# 设置 ANDROID_HOME 环境变量
# 运行 ./gradlew assembleDebug
```

## 项目结构

```
WorkHourTracker/
├── app/src/main/
│   ├── java/com/workhour/tracker/
│   │   ├── MainActivity.java          # 主界面
│   │   ├── CalendarAdapter.java       # 日历适配器
│   │   ├── SettingsManager.java       # 设置管理
│   │   └── WorkHourDataManager.java   # 数据管理
│   ├── res/layout/
│   │   ├── activity_main.xml          # 主界面布局
│   │   ├── dialog_settings.xml        # 设置弹窗布局
│   │   └── item_calendar_day.xml      # 日历日期项
│   └── AndroidManifest.xml
├── .github/workflows/build.yml        # GitHub Actions 构建配置
└── build.gradle
```
