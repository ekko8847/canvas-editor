# 自定义插件

::: warning
目前仅支持对编辑器实例进行方法的增加及修改，后续扩展更多功能
:::

## 开发插件

```javascript
export function myPlugin(editor: Editor, options?: Option) {
  // 1. 修改方法，详见：src/plugins/copy
  editor.command.updateFunction = () => {}

  // 2. 增加方法，详见：src/plugins/markdown
  editor.command.addFunction = () => {}
}
```

## 使用插件

```javascript
instance.add(myPlugin, options?: Option)
```