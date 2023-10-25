
---
share: true

---
# 简介

Bifrons 是一个开源、轻量、高效、跨语言、<del>可拓展</del>的矢量图像 / 卡片生成器

Bifrons 基于 cairo 与 OpenGL 来处理图像和矢量对象，以xml的规范输出，或转换成图片或网页组件

Bifrons 预计会支持Python、Java、Go、js、C#等SDK封装

Bifrons 是面向那些需要快速构建图片卡片，或者需要比svg更高级的功能所设计的，Bifrons在这些场景比 playwright 更轻量、快速，比svg语法更简洁，适合生成需要高效阅览、效果更好的图片或网页组件。

# 使用

- preconstruct_0
```python
import bifrons

card = bifrons.Card((640, 480))
style = bifrons.Style(
	horizon_align_self='center',
	vertical_align_self='center'
)
card.add(bifrons.Text('Hello World!', style))

# card.render()  # -> PNG ByteIO
card.show()
```

- preconstruct_1
```python
import bifrons

card = bifrons.Card((640, 480))
style_text = bifrons.Style(
	bifrons.style.horizon_align_self('center'),
	bifrons.style.vertical_align_self('center')
)
card.add(bifrons.Text('Hello World!', style))

# card.render()  # -> PNG ByteIO
card.show()
```
