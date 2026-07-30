# WGSL Literal Enhanced

[English](./README.md) | [简体中文](./README.zh-CN.md)

本扩展是基于 [gsimone/vscode-wgsl-literal](https://github.com/gsimone/vscode-wgsl-literal)（[Marketplace：`ggsimm.wgsl-literal`](https://marketplace.visualstudio.com/items?itemName=ggsimm.wgsl-literal)）的 **fork 增强版**。

在保留原版 `/* wgsl */` 模板字符串高亮能力的基础上，扩展到更多宿主语言：**JavaScript、TypeScript、TSX、Vue、HTML、Markdown**。

## 功能

- 为 `/* wgsl */ \`...\`` 模板字符串提供 WGSL 语法高亮
- 支持 `.js` / `.mjs` / `.ts` / `.tsx` / `.vue` / `.html` / `.md`
- Markdown 中支持 ` ```wgsl ` 围栏代码块
- 兼容新版 **Vue - Official**（`text.html.vue`）以及旧版 `source.vue` 语法作用域

## 依赖

请安装 [WGSL](https://marketplace.visualstudio.com/items?itemName=PolyMeilex.wgsl) 扩展（`PolyMeilex.wgsl`）。本扩展依赖其提供的 `source.wgsl` 语法。

## 用法

在模板字符串前加上 `/* wgsl */` 注释即可：

```js
const shader = /* wgsl */ `
  @vertex fn vs(
    @builtin(vertex_index) vertexIndex : u32
  ) -> @builtin(position) vec4f {
    return vec4f(0.0, 0.0, 0.0, 1.0);
  }
`;
```

在 Markdown 中也可以使用 WGSL 围栏代码块：

````md
```wgsl
@fragment fn fs() -> @location(0) vec4f {
  return vec4f(1.0, 0.0, 0.0, 1.0);
}
```
````

## 示例

### JavaScript / TypeScript

<img src="./image/js.png" alt="JavaScript / TypeScript" width="300" />

### TSX

<img src="./image/tsx.png" alt="TSX" width="480" />

### Vue

<img src="./image/vue.png" alt="Vue" width="300" />

### HTML

<img src="./image/html.png" alt="HTML" width="300" />

### Markdown

<img src="./image/md.png" alt="Markdown" width="300" />

## 致谢

基于 [gsimone](https://github.com/gsimone) 及贡献者开发的原版 [vscode-wgsl-literal](https://github.com/gsimone/vscode-wgsl-literal)。本 fork 在保留原有注释写法的同时，扩展了 Vue、HTML、Markdown、TSX 等语言的注入高亮支持。
