# SCLI
搜狗知音跨平台客户端

## 帮助文档

见 [https://docs.zhiyin.sogou.com/docs/scli](https://docs.zhiyin.sogou.com/docs/scli)

## Release Notes

v1.2.2:
- 增加流式合成命令支持
- BUGFIX：没有特定文件命令无法执行

v1.2.0：
- 语音识别、合成支持 pipe：
```bash
$ fmedia --record --format=int16 --rate=16000 --channels=mono --out=@stdout.wav 2>/dev/null | scli asr streaming-recognize --quiet
{"results":[{"alternatives":[{"transcript":"今天"}]}]}
{"results":[{"alternatives":[{"transcript":"今天天气"}]}]}
{"results":[{"alternatives":[{"transcript":"今天天气不错。","confidence":1}],"is_final":true}]}
{"results":[{"alternatives":[{"transcript":"明天"}]}]}
{"results":[{"alternatives":[{"transcript":"明天天气"}]}]}
{"results":[{"alternatives":[{"transcript":"明天天气怎么样？","confidence":0.99993896}],"is_final":true}]}
```

v1.1.9：
- 对外发布

v1.0.0 ~ 1.1.8:
- 内部开发 & 使用
