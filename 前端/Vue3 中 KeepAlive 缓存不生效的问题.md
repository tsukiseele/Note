# Vue3 中 KeepAlive 缓存不生效的问题

> 更新到 Vue3 之后，`<KeepAlice/>`必须配合`<Component/>`使用才能正常生效，导致 Vue2 的方法不再适用

### Vue2 的配置

```js
main#main
  KeepAlive
    RouterView
```

### Vue3 的配置

```js
main#main
  RouterView(v-slot="{ Component }")
    KeepAlive
      Component(:is="Component")
```

