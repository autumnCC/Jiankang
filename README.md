#血压助手(BP Recorder-Health Assistant)

## 项目结构
本项目采用 MVVM 架构，文件结构如下：

## 启动说明

1. **添加文件到 Xcode**:
   - 打开 `Jiankang.xcodeproj`。
   - 在左侧项目导航栏中，右键点击 `Jiankang` 文件夹。
   - 选择 "Add Files to 'Jiankang'..."。
   - 选中 `Models`, `Views`, `ViewModels`, `Services`, `Utils` 文件夹并添加。

2. **配置 HealthKit**:
   - 点击项目根节点 `Jiankang`。
   - 选择 Target `Jiankang`。
   - 进入 "Signing & Capabilities" 选项卡。
   - 点击 "+ Capability"，搜索并添加 "HealthKit"。
   - *注意*：已在项目配置中自动添加了 HealthKit 权限和隐私描述。如遇权限问题，请检查 Info.plist 设置。

3. **运行**:
   - 选择模拟器或真机运行。
   - 首次启动会弹出隐私政策，同意后请求 HealthKit 权限。

## 功能列表
- **记录**: 支持血压（滚轮选择）和血糖（场景选择）记录。
- **统计**: 7/30天趋势图，异常高亮。
- **设置**: 单位切换 (mmHg/kPa, mmol/L/mg/dL)，数据导出 CSV，每日提醒。
- **同步**: 自动同步数据到 Apple Health (需授权)。
