name: 🎵 歌曲请求
description: 请求添加新的歌曲到示例音乐库
title: "[Song Request] 歌曲名称 - 歌手"
labels: ["song-request"]
body:
  - type: markdown
    attributes:
      value: |
        **感谢你为 SLMusicFetch 提出歌曲请求！**  
        请尽量完整填写以下内容，帮助我们更好地评估和添加歌曲。

  - type: input
    id: song-info
    attributes:
      label: 歌曲名称 + 歌手
      description: 请填写完整的歌曲名称和歌手（例如：稻香 - 周杰伦）
      placeholder: 稻香 - 周杰伦
    validations:
      required: true

  - type: input
    id: song-link
    attributes:
      label: 歌曲链接（强烈推荐）
      description: 网易云音乐、Bilibili 的可公开访问的链接
      placeholder: https://...
    validations:
      required: false

  - type: textarea
    id: reason
    attributes:
      label: 你为什么要添加这首歌？
      description: 请说明理由，例如：这首歌很经典、适合某个场景、能丰富音乐库的风格等。
      placeholder: 这首歌是周杰伦的经典作品，在游戏中作为背景音乐氛围很好...
    validations:
      required: true

  - type: checkboxes
    id: contribute
    attributes:
      label: 你愿意提交 PR 吗？
      description: 如果你愿意帮忙提交 PR（提供音频文件或元数据），请勾选。
      options:
        - label: 我愿意提交 PR 来帮助添加这首歌
          required: false

  - type: textarea
    id: extra-info
    attributes:
      label: 其他信息（可选）
      description: 音乐风格、语言、年代、特殊备注等
      placeholder: 风格：华语流行 / 语言：中文 / 年代：2000s
    validations:
      required: false
