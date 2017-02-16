<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [dnsadminv2 api](#dnsadminv2-api)
- [缓存组接口](#%E7%BC%93%E5%AD%98%E7%BB%84%E6%8E%A5%E5%8F%A3)
  - [新建缓存组](#%E6%96%B0%E5%BB%BA%E7%BC%93%E5%AD%98%E7%BB%84)
  - [获取缓存组列表](#%E8%8E%B7%E5%8F%96%E7%BC%93%E5%AD%98%E7%BB%84%E5%88%97%E8%A1%A8)
  - [删除缓存组](#%E5%88%A0%E9%99%A4%E7%BC%93%E5%AD%98%E7%BB%84)
  - [缓存组增加ip](#%E7%BC%93%E5%AD%98%E7%BB%84%E5%A2%9E%E5%8A%A0ip)
  - [缓存组删除ip](#%E7%BC%93%E5%AD%98%E7%BB%84%E5%88%A0%E9%99%A4ip)
  - [修改缓存组自动人工模式](#%E4%BF%AE%E6%94%B9%E7%BC%93%E5%AD%98%E7%BB%84%E8%87%AA%E5%8A%A8%E4%BA%BA%E5%B7%A5%E6%A8%A1%E5%BC%8F)
  - [修改缓存组人工上下线](#%E4%BF%AE%E6%94%B9%E7%BC%93%E5%AD%98%E7%BB%84%E4%BA%BA%E5%B7%A5%E4%B8%8A%E4%B8%8B%E7%BA%BF)
- [zone域名接口](#zone%E5%9F%9F%E5%90%8D%E6%8E%A5%E5%8F%A3)
  - [获取域名列表](#%E8%8E%B7%E5%8F%96%E5%9F%9F%E5%90%8D%E5%88%97%E8%A1%A8)
- [调度平台接口](#%E8%B0%83%E5%BA%A6%E5%B9%B3%E5%8F%B0%E6%8E%A5%E5%8F%A3)
  - [新增调度平台域名记录](#%E6%96%B0%E5%A2%9E%E8%B0%83%E5%BA%A6%E5%B9%B3%E5%8F%B0%E5%9F%9F%E5%90%8D%E8%AE%B0%E5%BD%95)
  - [获取调度平台列表](#%E8%8E%B7%E5%8F%96%E8%B0%83%E5%BA%A6%E5%B9%B3%E5%8F%B0%E5%88%97%E8%A1%A8)
  - [增加域名区域覆盖缓存组(增加临时借用也是这个接口)](#%E5%A2%9E%E5%8A%A0%E5%9F%9F%E5%90%8D%E5%8C%BA%E5%9F%9F%E8%A6%86%E7%9B%96%E7%BC%93%E5%AD%98%E7%BB%84%E5%A2%9E%E5%8A%A0%E4%B8%B4%E6%97%B6%E5%80%9F%E7%94%A8%E4%B9%9F%E6%98%AF%E8%BF%99%E4%B8%AA%E6%8E%A5%E5%8F%A3)
  - [删除域名区域覆盖下缓存组](#%E5%88%A0%E9%99%A4%E5%9F%9F%E5%90%8D%E5%8C%BA%E5%9F%9F%E8%A6%86%E7%9B%96%E4%B8%8B%E7%BC%93%E5%AD%98%E7%BB%84)
  - [修改区域覆盖的缓存组使用信息(暂停/恢复,修改权重)](#%E4%BF%AE%E6%94%B9%E5%8C%BA%E5%9F%9F%E8%A6%86%E7%9B%96%E7%9A%84%E7%BC%93%E5%AD%98%E7%BB%84%E4%BD%BF%E7%94%A8%E4%BF%A1%E6%81%AF%E6%9A%82%E5%81%9C%E6%81%A2%E5%A4%8D%E4%BF%AE%E6%94%B9%E6%9D%83%E9%87%8D)
- [接入层接口](#%E6%8E%A5%E5%85%A5%E5%B1%82%E6%8E%A5%E5%8F%A3)
  - [新增接入层域名记录](#%E6%96%B0%E5%A2%9E%E6%8E%A5%E5%85%A5%E5%B1%82%E5%9F%9F%E5%90%8D%E8%AE%B0%E5%BD%95)
  - [删除接入层域名记录](#%E5%88%A0%E9%99%A4%E6%8E%A5%E5%85%A5%E5%B1%82%E5%9F%9F%E5%90%8D%E8%AE%B0%E5%BD%95)
  - [获取接入层域名列表](#%E8%8E%B7%E5%8F%96%E6%8E%A5%E5%85%A5%E5%B1%82%E5%9F%9F%E5%90%8D%E5%88%97%E8%A1%A8)
  - [修改接入层域名记录](#%E4%BF%AE%E6%94%B9%E6%8E%A5%E5%85%A5%E5%B1%82%E5%9F%9F%E5%90%8D%E8%AE%B0%E5%BD%95)
  - [获取view列表](#%E8%8E%B7%E5%8F%96view%E5%88%97%E8%A1%A8)
  - [获取view列表](#%E8%8E%B7%E5%8F%96view%E5%88%97%E8%A1%A8-1)
  - [operation log记录确认](#operation-log%E8%AE%B0%E5%BD%95%E7%A1%AE%E8%AE%A4)
  - [platform record列表](#platform-record%E5%88%97%E8%A1%A8)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


dnsadminv2 api
==============

# 缓存组接口
## 新建缓存组

请求包

```
POST /v2/groups
{
	"group_name":"bj_changping_all_cnc",
	"ips":["1.1.1.1","2.2.2.2"],
	"comment":"xxxxxx"
}
```

返回包

```
{
  "code": 200,
  "error": ""
}
```


## 获取缓存组列表

请求包
```
GET /v2/groups
```

返回包

```
{
  "code": 200,
  "error": "",
  "data": [
    {
      "id": 1,
      "name": "bj_changping_all_cnc",
      "mode":"auto",
      "status": "online",
      "comment":"xxxx"
      "ips"[
        {
            "ip":"157.255.158.79",
            "status":"online"
        }
      ]
    }
  ]
}
```

## 删除缓存组

请求包

```
DELETE /v2/groups/:id

{
	"op_reason":"xxxxxx"
}
```

返回包

```
{
  "code": 200,
  "error": ""
}
```


## 缓存组增加ip

请求包

```
POST /v2/groups/:id/ips
{
	"ips":["1.1.1.1","2.2.2.2"],
	"op_reason":"xxxxxx"
}
```

返回包

```
{
  "code": 200,
  "error": ""
}
```

## 缓存组删除ip

请求包

```
DELETE /v2/groups/:id/ips
{
	"ips":["1.1.1.1","2.2.2.2"],
	"comment":"xxxxxx"
}
```

返回包

```
{
  "code": 200,
  "error": ""
}
```

## 修改缓存组自动人工模式

请求包

```
POST /v2/groups/:id/mode
{
	"mode":"auto",              //取值是 "auto","manual"
	"op_reason":"xxxxxx"
}
```

返回包

```
{
  "code": 200,
  "error": ""
}
```


## 修改缓存组人工上下线

请求包

```
POST /v2/groups/:id/status
{
	"status":"online",              //取值是 "online","offline"
	"op_reason":"xxxxxx"
}
```

返回包

```
{
  "code": 200,
  "error": ""
}
```

##接受监控信息接口

```
POST /v2/:ip/status
{
    "status":"online"    //取值是 "online","offline"
}
```

# zone域名接口

##新增域名
请求包
```
POST /v2/zones
{
    "name": "qnydns.com",
}
```

返回包

```
{
  "code": 200,
  "error": ""
}
```

## 获取域名列表

请求包
```
GET /v2/zones
```

返回包

```
{
  "code": 200,
  "error": "",
  "data": [
    {
      "id": 1,
      "name": "qnydns.com",
      "status": "online"
    }
  ]
}
```


# 调度平台接口

## 新增调度平台域名记录

请求包
```
POST /v2/platforms
{
    "name": "all.lv2",
    "zone_id": 1
}
```

返回包

```
{
  "code": 200,
  "error": ""
}
```

## 获取调度平台列表

请求包
```
GET /v2/platforms
```

返回包

```
{
  "code": 200,
  "error": "",
  "data": [
    {
      "id": 1,
      "name": "all.lv2",
      "zone_name":"qnydns.com",
      "status": "online"
    }
  ]
}
```

## 增加域名区域覆盖缓存组(增加临时借用也是这个接口)

请求包

```
POST /v2/platforms/:id/views/:view_id
{
	"group_id":1,
	"weight":50,
	"use_type":"temporary"     //取值为 "temporary":临时借用，"permanent":正常增加
	"op_reason":"xxx"
}
```

返回包

```
{
  "code": 200,
  "error": ""
}
```

## 删除域名区域覆盖下缓存组

请求包

```
DELETE /v2/platforms/:id/views/:view_id
{
	"group_id":1,
	"op_reason":"xxx"
}
```

返回包

```
{
  "code": 200,
  "error": ""
}
```

## 修改区域覆盖的缓存组使用信息(暂停/恢复,修改权重)

请求包

```
PUT /v2/platforms/:id/views/:view_id/groups/:group_id
{
	"status":"online",  //取值有 "online","offline"
	"weight":10,
	"op_reason":"xxx"
}
```

返回包

```
{
  "code": 200,
  "error": ""
}
```

# 接入层接口

## 新增接入层域名记录

请求包

```
POST /v2/joints
{
	"name" : "all.china.qiniu",
	"zone_id" : 1,
	"platform_id" : 2
}
```

返回包

```
{
  "code": 200,
  "error": ""
}
```


## 删除接入层域名记录

请求包

```
DELETE /v2/joints/:id
{
	"op_reason" : "xxx",
}
```

返回包

```
{
  "code": 200,
  "error": ""
}
```

## 获取接入层域名列表

请求包
```
GET /v2/joints
```

返回包

```
{
  "code": 200,
  "error": "",
  "data": [
    {
      "id": 1,
      "name": "all.china.qiniu",
      "platform":"all.lv2.qnydns.com",
      "status": "online"
    }
  ]
}
```



## 修改接入层域名记录

请求包

```
PUT /v2/joints/:id
{
    "platform_id":1,
    "status":"online",     //取值为 "online","offline"
	"op_reason" : "xxx"
}
```

返回包

```
{
  "code": 200,
  "error": ""
}
```


## 获取view列表

请求包

```
GET /v2/views
```

返回包

```
{
  "code": 200,
  "error": "",
  "data": [
    {
       "id":1,
       "view":"北京联通"，
       "parent_id":12,
       "view_level":1
    }
  ]
}
```



## 获取view列表

请求包

```
GET /v2/operationlogs?page=1&&per_page=100
```

返回包

```
{
  "code": 200,
  "error": "",
  "data": [
    {
      "id":1,
      "method":"POST",
      "user": "xxxx",
      "value": "",
      "created_utc":"2016-12-23 11:54:20",
      "status": "confirmed",
      "confirm_utc":"2016-12-23 11:54:20"
    }
  ]
}
```


## operation log记录确认

请求包

```
POST /v2/operationlogs/:id
{
	"status": "confirmed"
}

```

返回包

```
{
  "code": 200,
  "error": ""
}
```

## platform record列表
请求包

```
GET /v2/platform/records?platform_id=1&page=1&&per_page=100

```

返回包

```
{
  "code": 200,
  "error": "",
  "data": [
    {
      "id": 3391,
      "domain": "all.lv200",
      "zone": "qnydns.com",
      "record_type": "A",
      "record_line": "上海移动",
      "value": "117.148.129.15",
      "mx": 0,
      "ttl": 139,
      "status": "enable",
      "weight": 40
    }
  ]
}
```
