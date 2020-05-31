# Alpine

[![Docker Automated Status](https://img.shields.io/docker/cloud/automated/docker4cn/debian.svg)](https://hub.docker.com/r/docker4cn/alpine/builds/)
[![Docker Build Status](https://img.shields.io/docker/cloud/build/docker4cn/debian.svg)](https://hub.docker.com/r/docker4cn/alpine/builds/)
[![Docker Stars](https://img.shields.io/docker/stars/docker4cn/debian.svg)](https://hub.docker.com/r/docker4cn/alpine/)
[![Docker Pulls](https://img.shields.io/docker/pulls/docker4cn/debian.svg)](https://hub.docker.com/r/docker4cn/alpine/)
[![License](https://img.shields.io/github/license/docker4cn/debian.svg)](https://github.com/yanqd0/docker4cn/alpine/master/LICENSE)

这是为中国定制的Debian镜像，上游是Docker官方的[alpine](https://hub.docker.com/_/alpine)。
它是[docker4cn]项目的一个部分。

[docker4cn]:https://docker-4.cn/

## 定制

Alpine镜像替换为以下源：

| 机构     | 源       | 域名                           | 信息链接                                           |
| ----     | --       | ----                           | --------                                           |
| 清华     | `tuna`   | `mirrors.tuna.tsinghua.edu.cn` | <https://mirror.tuna.tsinghua.edu.cn/help/alpine/> |
| 中科大   | `ustc`   | `mirrors.ustc.edu.cn`          | <https://mirrors.ustc.edu.cn/>                     |
| 阿里巴巴 | `aliyun` | `mirrors.aliyun.com`           | <https://developer.aliyun.com/mirror/>             |
| 华为     | `huawei` | `mirrors.huaweicloud.com`      | <https://mirrors.huaweicloud.com/>                 |

除了换源，还做了以下改进：

- 预装`ca-certificates`证书包，使用`https`的方式下载软件包。
- 设置时区为中国的`+8`区（`Asia/Shanghai`）。
- 增加PyPI、NPM、Gradle的镜像或代理。

## 使用示例

镜像tag的规则是`<版本>-<中国源>`。

```sh
docker pull docker4cn/alpine:3.12-aliyun
```

默认`lastest`使用`tuna`，因为它是Alpine官网展示的首个中国区镜像。
目前的`latest`是`3.12-tuna`，但它通常不是最合适的源，推荐通过tag选择特定镜像。
通过`ping <域名>`，找到最近的源，往往会有更好的使用效果。

已支持版本：

- 3.12
- 3.11
- 3.10

## 其它

更多docker4cn定制Docker基础镜像，请访问：<https://docker-4.cn/>

更多Alpine镜像，参考：[Official Alpine Linux mirrors](https://mirrors.alpinelinux.org/)。

如果希望更新、改进，请提[issues]或PR。

[issues]:https://github.com/docker4cn/debian/issues/new
