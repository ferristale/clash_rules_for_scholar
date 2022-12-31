# clash_rules_for_scholar
提供了一些和学术相关的网址以方便分流。对于大部分学术网站来说，需要使用订阅了相关权限的学校 ip 访问才能获得完整的内容。

来源：@nerdneilsfield and @ihel1 的scholar规则，修订后删除国内网站。

使用了 `cdn.jsdelivr.net` 的 CDN:



## 使用方法

将CFW自带的`Parsers`修改如下，更新订阅即可

```yaml
parsers:
- reg: ^.*$     ## 匹配所有订阅

  yaml:

    prepend-rules:
      - RULE-SET,scholar,DIRECT
      
    mix-rule-providers:
        scholar: {type: http, behavior: classical, url: "https://cdn.jsdelivr.net/gh/ferristale/clash_rules_for_scholar/rules/scholar.yaml", path: ./Ruleset/scholar.yaml, interval: 86400}
```

