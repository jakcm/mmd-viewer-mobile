# MMD 模型查看器（移动端）

基于 Three.js 的 MMD（MikuMikuDance）模型查看器，支持模型跳舞动画和音乐播放，专为移动端触控优化。

## 功能

- 🎮 **MMD 模型加载** — 支持 .pmd / .pmx / .pmc 格式
- 💃 **舞蹈动画** — 加载 VMD 舞蹈动作，模型自动跳舞
- 🎵 **音乐播放** — 音频与动画同步播放
- 🔄 **模型切换** — 内置初音ミク + YYB式幻晓伊，支持导入本地模型
- 📱 **移动端优化** — 触摸旋转/缩放/平移，毛玻璃 UI，响应式布局
- 🎨 **描边渲染** — OutlineEffect 实现 MMD 风格描边
- 💡 **动态光照** — 聚光灯跟随模型 + 方向光阴影

## 内置模型

| 模型 | 格式 | 来源 |
|------|------|------|
| 初音ミク (miku_v2.pmd) | PMD | three.js r87 示例资源 |
| YYB式幻晓伊ver1.0 | PMX | 邮件附件 |

## 使用方法

### 本地运行

```bash
cd /Users/admin/projects/mmd-viewer-mobile
python3 -m http.server 8090
# 浏览器打开 http://localhost:8090
```

### 操作说明

1. **选择模型** — 点击右上角菜单按钮，在下拉列表中选择模型
2. **播放** — 点击「播放」按钮开始舞蹈动画 + 音乐
3. **暂停/恢复** — 点击「暂停」按钮
4. **停止** — 点击「停止」按钮，重置到初始姿态
5. **旋转视角** — 单指拖动旋转模型
6. **缩放** — 双指捏合缩放
7. **平移** — 双指拖动平移视角
8. **导入模型** — 点击「导入本地 MMD 模型」上传 .pmd/.pmx 文件

## 技术栈

- **Three.js** v0.171.0（最后包含 MMDLoader 的版本）
- **MMDLoader** — MMD 模型/动画加载器
- **MMDAnimationHelper** — 动画 + 音频同步
- **OutlineEffect** — MMD 描边效果
- **OrbitControls** — 移动端触摸控制
- **Ammo.js** — MMD 物理模拟引擎

## 项目结构

```
mmd-viewer-mobile/
├── index.html              # 主页面（单文件应用）
├── README.md               # 本文档
├── libs/
│   └── ammo.js             # Ammo.js 物理引擎
├── models/
│   ├── miku_v2.pmd         # 初音ミク 模型
│   ├── eyeM2.bmp          # 初音ミク 眼睛纹理
│   └── YYB式幻晓伊ver1.0.pmx  # YYB式幻晓伊 模型
├── vmd/
│   └── wavefile_v2.vmd     # 舞蹈动作数据
└── audio/
    └── wavefile_short.mp3  # 背景音乐
```

## 注意事项

- Three.js v0.172.0 起移除了 MMDLoader，本项目使用 v0.171.0
- 移动端浏览器需要用户点击才能播放音频（浏览器自动播放策略）
- VMD 舞蹈动画使用标准 MMD 骨骼命名，兼容不同模型
- PMX 模型的纹理文件需与模型在同一目录下

## 资源许可

模型、舞蹈、音频数据均来自 three.js 示例资源，遵循其原始许可。
YYB式幻晓伊模型由用户提供。