# 人生 K 线视频 Skill

把一个人的重要经历写成一条逐步生长的 K 线：起落、横盘、转折和结局，都由人生事件推动。这个项目面向支持 Agent Skills 的 AI 助手，包含创作指引、动画模板和本地渲染脚本。

## 灵感与样片

这个项目来自一种在抖音等短视频平台流行的表达：用 K 线讲名人的一生，把重大经历变成行情起伏。这类作品中有几十万到百万级播放的案例。我参考这种叙事方式，复刻并整理成一个可反复使用的 skill。

我发布的样片：[观看 YouTube Shorts](https://www.youtube.com/shorts/_Ol2V2QAvrY)

播放表现会受选题、文案、制作和分发影响，本项目提供的是创作与制作工具，不承诺流量结果。

## 安装

```bash
npx skills add linxumoney/life-kline
```

可用于支持 Skills 的 Agent。生成视频需要本机安装 Python、FFmpeg，以及 Playwright Chromium。

```bash
pip install -r requirements.txt
python -m playwright install chromium
```

## 快速开始

复制并修改 `assets/example.json`，然后运行：

```bash
python scripts/render.py --spec /path/to/spec.json --out /path/to/video.mp4
```

默认输出竖屏 720×1280、30fps 视频。可用 `--fps` 调整帧率；FFmpeg 不在系统 PATH 时传入 `--ffmpeg`。

长视频需要按实际分节数量调整时间轴和镜头计算，避免沿用短样片的固定时长。

## 文件说明

- `SKILL.md`：人物研究、节奏规划、K 线叙事、声音设计和验收指引。
- `assets/index.html`：Canvas 动画模板。
- `assets/example.json`：带公开史料来源的示例参数。
- `scripts/render.py`：本地渲染器，输出视频和抽查帧。

K 线数值是叙事隐喻，不是历史数据，也不是对人物的客观评分。声音为可选项；若按走势设计声音，音高应跟随同一条价格曲线平滑起伏。未经用户授权的参考音轨不会被打包进项目。

## 版权与许可

版权归 **林序聊AI（linxu聊AI）** 所有，代码与文档采用 MIT License，详见 [LICENSE](LICENSE)。示例中的史实来源列在 JSON 文件里。使用者需自行确认后续添加的素材、音频和资料具有适当使用权。
