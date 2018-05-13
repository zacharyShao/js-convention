# 关于http请求库的讨论

## fetch
- 需要自己做一定的封装，比如baseUrl，cancelRequest等
- 需要配备一个polyfill，fetch-polyfill 0.8.2版本压缩包6KB

## axios
- 0.18.0版本压缩包12.6KB
- 需要引入qs库，6.5.2版本9KB，但会增加query字符串的处理能力

## 关于最新标准的考虑
- 如果fetch成熟稳定，那么axios一定会出fetch版本，无缝迁移