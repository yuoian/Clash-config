function main(config) {
  config["proxy-groups"] = [
    {
      name: "节点选择",
      type: "select",
      icon: "https://img.icons8.com/?size=100&id=ooUU44cZMaFE&format=png&color=000000",
      "exclude-filter": "(?i)GB|Traffic|Expire|Premium|频道|订阅|ISP|流量|到期|过期|套餐|重置|官网|落地|http|关注|群组",
      proxies: ["自动选择", "全部节点", "香港自动", "新加坡自动", "日本自动", "美国自动", "小众自动"],
    },
    {
      name: "自动选择",
      type: "url-test",
      icon: "https://raw.githubusercontent.com/Vbaethon/HOMOMIX/main/Icon/Color/Large/Auto_Link.png",
      tolerance: 70,
      interval: 300,
      "include-all": true,
      "exclude-filter": "(?i)GB|Traffic|Expire|Premium|频道|订阅|ISP|流量|到期|过期|套餐|重置|官网|落地|http|关注|群组"
    },
    {
      name: "全部节点",
      type: "select",
      "include-all": true,
      icon: "https://raw.githubusercontent.com/Vbaethon/HOMOMIX/main/Icon/Color/Large/Global.png",
      "exclude-filter": "(?i)GB|Traffic|Expire|Premium|频道|订阅|ISP|流量|到期|过期|套餐|重置|官网|落地|http|关注|群组"
    },
    {
      name: "Emby",
      type: "select",
      proxies: ["自动选择", "全部节点", "香港自动", "新加坡自动", "日本自动", "美国自动", "小众自动"],
      icon: "https://img.icons8.com/?size=100&id=FHnoYAFmyvu0&format=png&color=000000"
    },
    {
      name: "国外媒体",
      type: "select",
      proxies: ["自动选择", "全部节点", "香港自动", "新加坡自动", "日本自动", "美国自动", "小众自动"],

      icon: "https://img.icons8.com/?size=100&id=F2R6V3ECtTmF&format=png&color=000000"
    },
    {
      name: "Google",
      type: "select",
      proxies: ["自动选择", "全部节点", "香港自动", "新加坡自动", "日本自动", "美国自动", "小众自动"],

      icon: "https://img.icons8.com/?size=100&id=17949&format=png&color=000000"
    },
    {
      name: "Telegram",
      type: "select",
      proxies: ["自动选择", "全部节点", "香港自动", "新加坡自动", "日本自动", "美国自动", "小众自动"],

      icon: "https://img.icons8.com/?size=100&id=63306&format=png&color=000000"
    },
    {
      name: "ChatGPT",
      type: "select",
      proxies: ["自动选择", "全部节点", "香港自动", "新加坡自动", "日本自动", "美国自动", "小众自动"],

      icon: "https://img.icons8.com/?size=100&id=FBO05Dys9QCg&format=png&color=000000"
    },
    {
      name: "Microsoft",
      type: "select",
      proxies: ["自动选择", "全部节点", "香港自动", "新加坡自动", "日本自动", "美国自动", "小众自动"],

      icon: "https://img.icons8.com/?size=100&id=22989&format=png&color=000000"
    },
    {
      name: "PayPal",
      type: "select",
      proxies: ["自动选择", "全部节点", "香港自动", "新加坡自动", "日本自动", "美国自动", "小众自动"],

      icon: "https://img.icons8.com/?size=100&id=13611&format=png&color=000000"
    },
    {
      name: "香港自动",
      type: "url-test",
      "include-all": true,
      filter: "(?i)港|hk|hongkong|hong kong",
      icon: "https://img.icons8.com/?size=100&id=WQgynbTLjuXX&format=png&color=000000"
    },
    {
      name: "新加坡自动",
      type: "url-test",
      "include-all": true,
      filter: "(?i)(新加坡|狮城|sg|singapore)",
      icon: "https://img.icons8.com/?size=100&id=8H-8FMObN4vB&format=png&color=000000"
    },
    {
      name: "日本自动",
      type: "url-test",
      "include-all": true,
      filter: "(?i)日|jp|japan",
      icon: "https://img.icons8.com/?size=100&id=McQbrq9qaQye&format=png&color=000000"
    },
    {
      name: "美国自动",
      type: "url-test",
      "include-all": true,
      filter: "(?i)美|美国|us|usa|unitedstates|united states|洛杉|俄亥俄",
      icon: "https://img.icons8.com/?size=100&id=aRiu1GGi6Aoe&format=png&color=000000"
    },
    {
      name: "小众自动",
      type: "url-test",
      "include-all": true,
      "exclude-filter": "(?i)GB|频道|订阅|流量|到期|过期|套餐|重置|官网|落地|http|关注|群组",
      filter:
        "(?i)^(?!.*(港|hk|hongkong|hong kong|新加坡|sg|singapore|日|jp|japan|美|美国|us|usa|unitedstates|united states|洛杉|俄亥俄)).*",
      icon: "https://img.icons8.com/?size=100&id=44028&format=png&color=000000"
    },
    {
      name: "Adblock",
      type: "select",
      proxies: ["REJECT", "DIRECT"],
      icon: "https://raw.githubusercontent.com/Vbaethon/HOMOMIX/main/Icon/Color/Large/AdblockPlus_2.png"
    },
    {
      name: "国内媒体",
      type: "select",
      proxies: ["DIRECT", "REJECT"],
      icon: "https://img.icons8.com/?size=100&id=d5TXEddDPJaA&format=png&color=000000"
    },
    {
      name: "国内直连",
      type: "select",
      proxies: ["DIRECT", "REJECT"],
      icon: "https://raw.githubusercontent.com/Vbaethon/HOMOMIX/main/Icon/Color/Large/DIRECT.png"
    }
  ];
  if (!config['rule-providers']) {
    config['rule-providers'] = {};
  }
  config["rule-providers"] = Object.assign(config["rule-providers"], {
    private: {
      url: "https://raw.githubusercontent.com/MetaCubeX/meta-rules-dat/meta/geo/geosite/private.mrs",
      path: "./ruleset/private.mrs",
      behavior: "domain",
      interval: 86400,
      format: "mrs",
      type: "http",
    },
    proxylite: {
      url: "https://raw.githubusercontent.com/qichiyuhub/rule/refs/heads/main/proxy.list",
      path: "./ruleset/proxylite.txt",
      behavior: "classical",
      interval: 86400,
      format: "text",
      type: "http",
    },
    ai: {
      url: "https://github.com/MetaCubeX/meta-rules-dat/raw/refs/heads/meta/geo/geosite/category-ai-!cn.mrs",
      path: "./ruleset/ai.mrs",
      behavior: "domain",
      interval: 86400,
      format: "mrs",
      type: "http",
    },
    cn_domain: {
      url: "https://testingcf.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@meta/geo/geosite/cn.mrs",
      path: "./ruleset/cn_domain.mrs",
      behavior: "domain",
      interval: 86400,
      format: "mrs",
      type: "http",
    },
    google_domain: {
      url: "https://testingcf.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@meta/geo/geosite/google.mrs",
      path: "./ruleset/google_domain.mrs",
      behavior: "domain",
      interval: 86400,
      format: "mrs",
      type: "http",
    },
    github_domain: {
      url: "https://testingcf.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@meta/geo/geosite/github.mrs",
      path: "./ruleset/github_domain.mrs",
      behavior: "domain",
      interval: 86400,
      format: "mrs",
      type: "http",
    },
    youtube_domain: {
      url: "https://testingcf.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@meta/geo/geosite/youtube.mrs",
      path: "./ruleset/youtube_domain.mrs",
      behavior: "domain",
      interval: 86400,
      format: "mrs",
      type: "http",
    },
    tiktok_domain: {
      url: "https://testingcf.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@meta/geo/geosite/tiktok.mrs",
      path: "./ruleset/tiktok_domain.mrs",
      behavior: "domain",
      interval: 86400,
      format: "mrs",
      type: "http",
    },
    telegram_domain: {
      url: "https://testingcf.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@meta/geo/geosite/telegram.mrs",
      path: "./ruleset/telegram_domain.mrs",
      behavior: "domain",
      interval: 86400,
      format: "mrs",
      type: "http",
    },
    netflix_domain: {
      url: "https://testingcf.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@meta/geo/geosite/netflix.mrs",
      path: "./ruleset/netflix_domain.mrs",
      behavior: "domain",
      interval: 86400,
      format: "mrs",
      type: "http",
    },
    paypal_domain: {
      url: "https://testingcf.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@meta/geo/geosite/paypal.mrs",
      path: "./ruleset/paypal_domain.mrs",
      behavior: "domain",
      interval: 86400,
      format: "mrs",
      type: "http",
    },
    microsoft_domain: {
      url: "https://testingcf.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@meta/geo/geosite/microsoft.mrs",
      path: "./ruleset/microsoft_domain.mrs",
      behavior: "domain",
      interval: 86400,
      format: "mrs",
      type: "http",
    },
    steam_domain: {
      url: "https://testingcf.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@meta/geo/geosite/steam.mrs",
      path: "./ruleset/steam_domain.mrs",
      behavior: "domain",
      interval: 86400,
      format: "mrs",
      type: "http",
    },
    gfw_domain: {
      url: "https://testingcf.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@meta/geo/geosite/gfw.mrs",
      path: "./ruleset/gfw_domain.mrs",
      behavior: "domain",
      interval: 86400,
      format: "mrs",
      type: "http",
    },
    "geolocation-!cn": {
      url: "https://testingcf.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@meta/geo/geosite/geolocation-!cn.mrs",
      path: "./ruleset/geolocation-!cn.mrs",
      behavior: "domain",
      interval: 86400,
      format: "mrs",
      type: "http",
    },
    china_media: {
      url: "https://testingcf.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@meta/geo/geosite/category-media-cn.mrs",
      path: "./ruleset/china_media.mrs",
      behavior: "domain",
      interval: 86400,
      format: "mrs",
      type: "http",
    },
    cn_ip: {
      url: "https://testingcf.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@meta/geo/geoip/cn.mrs",
      path: "./ruleset/cn_ip.mrs",
      behavior: "ipcidr",
      interval: 86400,
      format: "mrs",
      type: "http",
    },
    google_ip: {
      url: "https://testingcf.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@meta/geo/geoip/google.mrs",
      path: "./ruleset/google_ip.mrs",
      behavior: "ipcidr",
      interval: 86400,
      format: "mrs",
      type: "http",
    },
    telegram_ip: {
      url: "https://testingcf.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@meta/geo/geoip/telegram.mrs",
      path: "./ruleset/telegram_ip.mrs",
      behavior: "ipcidr",
      interval: 86400,
      format: "mrs",
      type: "http",
    },
    netflix_ip: {
      url: "https://testingcf.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@meta/geo/geoip/netflix.mrs",
      path: "./ruleset/netflix_ip.mrs",
      behavior: "ipcidr",
      interval: 86400,
      format: "mrs",
      type: "http",
    },
    adblock_domain: {
      url: "https://testingcf.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@meta/geo/geosite/category-ads-all.mrs",
      path: "./ruleset/adblock_domain.mrs",
      behavior: "domain",
      interval: 86400,
      format: "mrs",
      type: "http",
    },
  });

  config["rules"] = [
    // 内网直连
    "RULE-SET,private,DIRECT",

    // 广告拦截
    "RULE-SET,adblock_domain,Adblock",

    // 特定服务域名
    "RULE-SET,ai,ChatGPT",
    "RULE-SET,github_domain,节点选择",
    "RULE-SET,youtube_domain,国外媒体",
    "RULE-SET,google_domain,Google",
    "RULE-SET,google_ip,Google",
    "RULE-SET,microsoft_domain,Microsoft",
    "RULE-SET,tiktok_domain,国外媒体",
    "RULE-SET,telegram_domain,Telegram",
    "RULE-SET,telegram_ip,Telegram",
    "RULE-SET,netflix_domain,国外媒体",
    "RULE-SET,netflix_ip,国外媒体",
    "RULE-SET,paypal_domain,PayPal",
    "RULE-SET,steam_domain,节点选择",

    // Emby 专属识别
    "DOMAIN-KEYWORD,emby,Emby",
    "DOMAIN-SUFFIX,xxx.xx,Emby",

    // 通用代理 + GFW 域名兜底代理
    "RULE-SET,proxylite,节点选择",
    "RULE-SET,gfw_domain,节点选择",

    // 国内域名 + IP 直连
    "RULE-SET,china_media,国内媒体",
    "RULE-SET,cn_domain,DIRECT",
    "RULE-SET,cn_ip,DIRECT",

    // 国外 IP 代理
    "RULE-SET,geolocation-!cn,节点选择",

    // 兜底策略
    "MATCH,节点选择"
  ];
  return config;
}
