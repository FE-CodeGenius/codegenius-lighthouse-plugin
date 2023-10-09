# @codegenius/lighthouse-plugin

运行 `lighthouse` 分析及收集 **Web** 应用的性能指标

## 安装

``` bash
npm i @codegenius/lighthouse-plugin -D
```

```javascript
import { defineConfig } from "code-genius";
import { lighthouseInstaller } from "@codegenius/lighthouse-plugin";

export default defineConfig({
  plugins: [
    lighthouseInstaller(),
  ],
});
```

## 使用

### 命令模式

```bash
# 分析及收集 **baidu** 应用的性能指标
codeg lighthouse --url https://www.baidu.com
```

| 选项                | 描述         |
| ------------------- | ------------ |
| --url \<url\> | Web 应用地址 |

### API 模式

```typescript
import { lighthouse } from "@codegenius/lighthouse-plugin";

(async () => {
  await lighthouse("https://www.baidu.com");
})();
```