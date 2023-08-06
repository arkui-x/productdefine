# 公共产品形态配置<a name="ZH-CN_TOPIC_0000001079317008"></a>

-   [简介](#section11660541593)
-   [配置仓目录结构](#section113275517516)
-   [产品配置示例](#section113275517517)
-   [添加部件示例](#section113275517518)

## 简介<a name="section11660541593"></a>

ArkUI-X产品形态定义

## 配置仓目录结构<a name="section113275517516"></a>

```sh
productdefine/common
├── base                          # 最小系统部件集合
│   └── standard_system.json      # 标准系统最小部件集合
└── products                      # 系统组件形态配置文件，配置文件名称与product name保持一致
    └── arkui-x.json              # SDK部件集合
```

## 产品配置示例<a name="section113275517517"></a>
```json
{
  "product_name": "arkui-x",      # 产品形态名称
  "device_company": "ohos",       # 产品形态厂商
  "target_cpu": "arm64",          # 产品形态支持的指令集
  "version": "3.0",               # 配置文件格式版本
  "type": "standard",             # 系统类型
  "subsystems": [                 # 产品的部件列表
    {}
  ]
}
```
配置文件中各字段的含义如下：

| 字段           | 含义                                                         |
| -------------- | ------------------------------------------------------------ |
| version        | 配置文件版本号，当前都填"3.0"。                              |
| product_name   | 形态名称，可以通过此字段值作为`build.sh --product-name`的参数来完成产品的编译。 |
| device_company | 形态厂商，默认均填"ohos"。                           |
| target_cpu     | 系统组件形态支持的指令集。 |
| type           | 轻量系统("mini")，小型系统("small")还是标准系统("standard")。 |
| subsystems     | 支持的子系统部件列表。 |

## 添加部件示例<a name="section113275517518"></a>
```json
 {
  "product_name": "arkui-x",
  "device_company": "ohos",
  "target_cpu": "arm64",
  "version": "3.0",
  "type": "standard",
  "subsystems": [                         # 产品的部件列表
    {
      "subsystem": "subsystem_name"，     # 子系统名
      "components": [                     # 部件列表
        { "component": "part_name" }      # 部件名
      ]
    }
  ]
 }
```
