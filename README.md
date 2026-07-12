# MMD 模型查看器

基于 Three.js 的移动端 MMD 模型查看器，支持 PMX/PMD 模型加载、VMD 舞蹈动画、音频同步播放、唇形同步等功能。

## 功能

- 支持 PMX/PMD 3D 模型加载
- 支持 VMD 舞蹈动画播放
- 音频与动画同步播放
- 待机 idle 动画循环
- Edge TTS 唇形同步
- 移动端触控操作（单指旋转、双指缩放平移）
- OutlineEffect 描边渲染
- 本地文件导入（模型/舞蹈/音频）
- 渲染参数实时调节

## 技术参考

- [MMDLoader-app](https://github.com/takahirox/MMDLoader-app) — Three.js MMD 模型加载器示例
- [Three.js MMDLoader](https://threejs.org/docs/#examples/en/loaders/MMDLoader) — Three.js 官方 MMD 加载器文档

## 技术栈

- [Three.js](https://threejs.org/) v0.171.0（MMDLoader 最后支持版本）
- Edge TTS 语音合成
- GitHub Pages 部署

## 部署

```bash
# 推送到 GitHub 自动部署到 GitHub Pages
git push origin main
```

## 许可

仅用于个人学习和研究。
