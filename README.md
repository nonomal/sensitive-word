# sensitive-word

[sensitive-word](https://github.com/houbb/sensitive-word) 基于 DFA 算法实现的高性能敏感词工具。

[![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.github.houbb/sensitive-word/badge.svg)](http://mvnrepository.com/artifact/com.github.houbb/sensitive-word)
[![Open Source Love](https://badges.frapsoft.com/os/v2/open-source.svg?v=103)](https://github.com/houbb/sensitive-word)
[![](https://img.shields.io/badge/license-Apache2-FF0080.svg)](https://github.com/houbb/sensitive-word/blob/master/LICENSE.txt)

如果有一些疑难杂症，可以加入：[技术交流群](https://mp.weixin.qq.com/s/rkSvXxiiLGjl3S-ZOZCr0Q)

[sensitive-word-admin](https://github.com/houbb/sensitive-word-admin) 是对应的控台的应用，目前功能处于初期开发中，MVP 版本可用。

## 创作目的

大家好，我是老马。

一直想实现一款简单好用敏感词工具，于是开源实现了这个工具。

基于 DFA 算法实现，目前敏感词库内容收录 6W+（源文件 18W+，经过一次删减）。

后期将进行持续优化和补充敏感词库，并进一步提升算法的性能。

v0.24.0 开始内置支持对敏感词的分类细化，不过工作量比较大，难免存在疏漏。

欢迎 PR 改进， github 提需求，或者加入技术交流群沟通吹牛！

## 特性

- 6W+ 词库，且不断优化更新

- 基于 fluent-api 实现，使用优雅简洁

- [基于 DFA 算法，性能为 7W+ QPS，应用无感](https://github.com/houbb/sensitive-word#benchmark)

- [支持敏感词的判断、返回、脱敏等常见操作](https://github.com/houbb/sensitive-word#%E6%A0%B8%E5%BF%83%E6%96%B9%E6%B3%95)

- [支持常见的格式转换](https://github.com/houbb/sensitive-word#%E6%9B%B4%E5%A4%9A%E7%89%B9%E6%80%A7)

全角半角互换、英文大小写互换、数字常见形式的互换、中文繁简体互换、英文常见形式的互换、忽略重复词等

- [支持敏感词检测、邮箱检测、数字检测、网址检测、IPV4等](https://github.com/houbb/sensitive-word#%E6%9B%B4%E5%A4%9A%E6%A3%80%E6%B5%8B%E7%AD%96%E7%95%A5)

- [支持自定义替换策略](https://github.com/houbb/sensitive-word#%E8%87%AA%E5%AE%9A%E4%B9%89%E6%9B%BF%E6%8D%A2%E7%AD%96%E7%95%A5)

- [支持用户自定义敏感词和白名单](https://github.com/houbb/sensitive-word#%E9%85%8D%E7%BD%AE%E4%BD%BF%E7%94%A8)

- [支持数据的数据动态更新（用户自定义），实时生效](https://github.com/houbb/sensitive-word#%E5%8A%A8%E6%80%81%E5%8A%A0%E8%BD%BD%E7%94%A8%E6%88%B7%E8%87%AA%E5%AE%9A%E4%B9%89)

- [支持敏感词的标签接口+内置分类实现](https://github.com/houbb/sensitive-word#%E6%95%8F%E6%84%9F%E8%AF%8D%E6%A0%87%E7%AD%BE)

- [支持跳过一些特殊字符，让匹配更灵活](https://github.com/houbb/sensitive-word#%E5%BF%BD%E7%95%A5%E5%AD%97%E7%AC%A6)

- [支持黑白名单单个的新增/修改，无需全量初始化](https://github.com/houbb/sensitive-word?tab=readme-ov-file#%E9%92%88%E5%AF%B9%E5%8D%95%E4%B8%AA%E8%AF%8D%E7%9A%84%E6%96%B0%E5%A2%9E%E5%88%A0%E9%99%A4%E6%97%A0%E9%9C%80%E5%85%A8%E9%87%8F%E5%88%9D%E5%A7%8B%E5%8C%96)

- [支持词匹配模式的两种模式](https://github.com/houbb/sensitive-word?tab=readme-ov-file#wordfailfast-%E6%95%8F%E6%84%9F%E8%AF%8D%E5%8C%B9%E9%85%8D%E5%BF%AB%E9%80%9F%E5%A4%B1%E8%B4%A5%E6%A8%A1%E5%BC%8F)

## 项目推荐

下面是一些日志、加解密、脱敏安全相关的库推荐：

| 项目                                                                    | 介绍                    |
|:----------------------------------------------------------------------|:----------------------|
| [sensitive-word](https://github.com/houbb/sensitive-word)             | 高性能敏感词核心库             |
| [sensitive-word-admin](https://github.com/houbb/sensitive-word-admin) | 敏感词控台，前后端分离           |
| [sensitive](https://github.com/houbb/sensitive)                       | 高性能日志脱敏组件             |
| [auto-log](https://github.com/houbb/auto-log)                         | 统一日志切面组件，支持全链路traceId |
| [encryption-local](https://github.com/houbb/encryption-local)         | 离线加密机组件               |
| [encryption](https://github.com/houbb/encryption)         | 加密机标准API+本地客户端        |
| [encryption-server](https://github.com/houbb/encryption-server)        | 加密机服务                 |

## 变更日志

[CHANGE_LOG.md](https://github.com/houbb/sensitive-word/blob/master/CHANGE_LOG.md)

## 更多资料

### 敏感词控台

有时候敏感词有一个控台，配置起来会更加灵活方便。

> [java 如何实现开箱即用的敏感词控台服务？](https://mp.weixin.qq.com/s/rQo75cfMU_OEbTJa0JGMGg)

### 敏感词标签文件

梳理了大量的敏感词标签文件，可以让我们的敏感词更加方便。

这两个资料阅读可在下方文章获取：

> [v0.11.0-敏感词新特性及对应标签文件](https://mp.weixin.qq.com/s/m40ZnR6YF6WgPrArUSZ_0g)

目前 v0.24.0 已内置实现单词标签，需要的建议升级到最新版本。

# 支持开源

开源不易，如果本项目对你有帮助，你可以请老马喝一杯奶茶。

<img src="https://github.com/houbb/sensitive-word/raw/master/lmxxf_reword.png?raw=true" style="width: 300px; height: 200px;"/>

# 快速开始

## 准备

- JDK1.8+

- Maven 3.x+

## Maven 引入

```xml
<dependency>
    <groupId>com.github.houbb</groupId>
    <artifactId>sensitive-word</artifactId>
    <version>0.27.0</version>
</dependency>
```

## 核心方法

`SensitiveWordHelper` 作为敏感词的工具类，核心方法如下：

注意：`SensitiveWordHelper` 提供的都是默认配置。如果你希望进行灵活的自定义配置，可参考 [引导类特性配置](https://github.com/houbb/sensitive-word/?tab=readme-ov-file#%E5%BC%95%E5%AF%BC%E7%B1%BB%E7%89%B9%E6%80%A7%E9%85%8D%E7%BD%AE)

| 方法                                     | 参数                       | 返回值    | 说明           |
|:---------------------------------------|:-------------------------|:-------|:-------------|
| contains(String)                       | 待验证的字符串                  | 布尔值    | 验证字符串是否包含敏感词 |
| replace(String, ISensitiveWordReplace) | 使用指定的替换策略替换敏感词           | 字符串    | 返回脱敏后的字符串    |
| replace(String, char)                  | 使用指定的 char 替换敏感词         | 字符串    | 返回脱敏后的字符串    |
| replace(String)                        | 使用 `*` 替换敏感词             | 字符串    | 返回脱敏后的字符串    |
| findAll(String)                        | 待验证的字符串                  | 字符串列表  | 返回字符串中所有敏感词  |
| findFirst(String)                      | 待验证的字符串                  | 字符串    | 返回字符串中第一个敏感词 |
| findAll(String, IWordResultHandler)    | IWordResultHandler 结果处理类 | 字符串列表  | 返回字符串中所有敏感词  |
| findFirst(String, IWordResultHandler)  | IWordResultHandler 结果处理类 | 字符串    | 返回字符串中第一个敏感词 |
| tags(String)       | 获取敏感词的标签                 | 敏感词字符串 | 返回敏感词的标签列表   |



### 判断是否包含敏感词

```java
final String text = "五星红旗迎风飘扬，毛主席的画像屹立在天安门前。";

Assert.assertTrue(SensitiveWordHelper.contains(text));
```

### 返回第一个敏感词

```java
final String text = "五星红旗迎风飘扬，毛主席的画像屹立在天安门前。";

String word = SensitiveWordHelper.findFirst(text);
Assert.assertEquals("五星红旗", word);
```

SensitiveWordHelper.findFirst(text) 等价于：

```java
String word = SensitiveWordHelper.findFirst(text, WordResultHandlers.word());
```

### 返回所有敏感词

```java
final String text = "五星红旗迎风飘扬，毛主席的画像屹立在天安门前。";

List<String> wordList = SensitiveWordHelper.findAll(text);
Assert.assertEquals("[五星红旗, 毛主席, 天安门]", wordList.toString());
```

返回所有敏感词用法上类似于 SensitiveWordHelper.findFirst()，同样也支持指定结果处理类。

SensitiveWordHelper.findAll(text) 等价于：

```java
List<String> wordList = SensitiveWordHelper.findAll(text, WordResultHandlers.word());
```

WordResultHandlers.raw() 可以保留对应的下标信息、类别信息：

```java
final String text = "五星红旗迎风飘扬，毛主席的画像屹立在天安门前。";

// 默认敏感词标签为空
List<WordTagsDto> wordList1 = SensitiveWordHelper.findAll(text, WordResultHandlers.wordTags());
Assert.assertEquals("[WordTagsDto{word='五星红旗', tags=[]}, WordTagsDto{word='毛主席', tags=[]}, WordTagsDto{word='天安门', tags=[]}]", wordList1.toString());
```

### 默认的替换策略

```java
final String text = "五星红旗迎风飘扬，毛主席的画像屹立在天安门前。";
String result = SensitiveWordHelper.replace(text);
Assert.assertEquals("****迎风飘扬，***的画像屹立在***前。", result);
```

### 指定替换的内容

```java
final String text = "五星红旗迎风飘扬，毛主席的画像屹立在天安门前。";
String result = SensitiveWordHelper.replace(text, '0');
Assert.assertEquals("0000迎风飘扬，000的画像屹立在000前。", result);
```

### 自定义替换策略

V0.2.0 支持该特性。

场景说明：有时候我们希望不同的敏感词有不同的替换结果。比如【游戏】替换为【电子竞技】，【失业】替换为【灵活就业】。

诚然，提前使用字符串的正则替换也可以，不过性能一般。

使用例子：

```java
/**
 * 自定替换策略
 * @since 0.2.0
 */
@Test
public void defineReplaceTest() {
    final String text = "五星红旗迎风飘扬，毛主席的画像屹立在天安门前。";

    ISensitiveWordReplace replace = new MySensitiveWordReplace();
    String result = SensitiveWordHelper.replace(text, replace);

    Assert.assertEquals("国家旗帜迎风飘扬，教员的画像屹立在***前。", result);
}
```

其中 `MySensitiveWordReplace` 是我们自定义的替换策略，实现如下：

```java
public class MyWordReplace implements IWordReplace {

    @Override
    public void replace(StringBuilder stringBuilder, final char[] rawChars, IWordResult wordResult, IWordContext wordContext) {
        String sensitiveWord = InnerWordCharUtils.getString(rawChars, wordResult);
        // 自定义不同的敏感词替换策略，可以从数据库等地方读取
        if("五星红旗".equals(sensitiveWord)) {
            stringBuilder.append("国家旗帜");
        } else if("毛主席".equals(sensitiveWord)) {
            stringBuilder.append("教员");
        } else {
            // 其他默认使用 * 代替
            int wordLength = wordResult.endIndex() - wordResult.startIndex();
            for(int i = 0; i < wordLength; i++) {
                stringBuilder.append('*');
            }
        }
    }

}
```

我们针对其中的部分词做固定映射处理，其他的默认转换为 `*`。

## IWordResultHandler 结果处理类

IWordResultHandler 可以对敏感词的结果进行处理，允许用户自定义。

内置实现见 `WordResultHandlers` 工具类：

- WordResultHandlers.word()

只保留敏感词单词本身。

- WordResultHandlers.raw()

保留敏感词相关信息，包含敏感词的开始和结束下标。

- WordResultHandlers.wordTags()

同时保留单词，和对应的词标签信息。

### 使用实例

所有测试案例参见 [SensitiveWordHelperTest](https://github.com/houbb/sensitive-word/blob/master/src/test/java/com/github/houbb/sensitive/word/core/SensitiveWordHelperTest.java)

1）基本例子

```java
final String text = "五星红旗迎风飘扬，毛主席的画像屹立在天安门前。";

List<String> wordList = SensitiveWordHelper.findAll(text);
Assert.assertEquals("[五星红旗, 毛主席, 天安门]", wordList.toString());
List<String> wordList2 = SensitiveWordHelper.findAll(text, WordResultHandlers.word());
Assert.assertEquals("[五星红旗, 毛主席, 天安门]", wordList2.toString());

List<IWordResult> wordList3 = SensitiveWordHelper.findAll(text, WordResultHandlers.raw());
Assert.assertEquals("[WordResult{startIndex=0, endIndex=4}, WordResult{startIndex=9, endIndex=12}, WordResult{startIndex=18, endIndex=21}]", wordList3.toString());
```

2) wordTags 例子

我们在 `dict_tag_test.txt` 文件中指定对应词的标签信息。

```java
final String text = "五星红旗迎风飘扬，毛主席的画像屹立在天安门前。";

// 默认敏感词标签为空
List<WordTagsDto> wordList1 = SensitiveWordHelper.findAll(text, WordResultHandlers.wordTags());
Assert.assertEquals("[WordTagsDto{word='五星红旗', tags=[]}, WordTagsDto{word='毛主席', tags=[]}, WordTagsDto{word='天安门', tags=[]}]", wordList1.toString());

List<WordTagsDto> wordList2 = SensitiveWordBs.newInstance()
        .wordTag(WordTags.file("dict_tag_test.txt"))
        .init()
        .findAll(text, WordResultHandlers.wordTags());
Assert.assertEquals("[WordTagsDto{word='五星红旗', tags=[政治, 国家]}, WordTagsDto{word='毛主席', tags=[政治, 伟人, 国家]}, WordTagsDto{word='天安门', tags=[政治, 国家, 地址]}]", wordList2.toString());
```

# 更多特性

后续的诸多特性，主要是针对各种针对各种情况的处理，尽可能的提升敏感词命中率。

这是一场漫长的攻防之战。

## 样式处理

### 忽略大小写

```java
final String text = "fuCK the bad words.";

String word = SensitiveWordHelper.findFirst(text);
Assert.assertEquals("fuCK", word);
```

### 忽略半角圆角

```java
final String text = "ｆｕｃｋ the bad words.";

String word = SensitiveWordHelper.findFirst(text);
Assert.assertEquals("ｆｕｃｋ", word);
```

### 忽略数字的写法

这里实现了数字常见形式的转换。

```java
final String text = "这个是我的微信：9⓿二肆⁹₈③⑸⒋➃㈤㊄";

List<String> wordList = SensitiveWordBs.newInstance().enableNumCheck(true).init().findAll(text);
Assert.assertEquals("[9⓿二肆⁹₈③⑸⒋➃㈤㊄]", wordList.toString());
```

### 忽略繁简体

```java
final String text = "我爱我的祖国和五星紅旗。";

List<String> wordList = SensitiveWordHelper.findAll(text);
Assert.assertEquals("[五星紅旗]", wordList.toString());
```

### 忽略英文的书写格式

```java
final String text = "Ⓕⓤc⒦ the bad words";

List<String> wordList = SensitiveWordHelper.findAll(text);
Assert.assertEquals("[Ⓕⓤc⒦]", wordList.toString());
```

### 忽略重复词

```java
final String text = "ⒻⒻⒻfⓤuⓤ⒰cⓒ⒦ the bad words";

List<String> wordList = SensitiveWordBs.newInstance()
        .ignoreRepeat(true)
        .init()
        .findAll(text);
Assert.assertEquals("[ⒻⒻⒻfⓤuⓤ⒰cⓒ⒦]", wordList.toString());
```

## 更多检测策略

### 说明

v0.25.0 目前的几个策略，也支持用户引导类自定义。所有的策略都是接口，支持用户自定义实现。

| 序号 | 方法                   | 说明                                         | 默认值   |
|:---|:---------------------|:-------------------------------------------|:------|
| 16 | wordCheckNum          | 数字检测策略(v0.25.0开始支持)                        | `WordChecks.num()`   |
| 17 | wordCheckEmail          | 邮箱检测策略(v0.25.0开始支持)                        | `WordChecks.email()`   |
| 18 | wordCheckUrl          | URL检测策略(v0.25.0开始支持)，内置还是实现了 `urlNoPrefix()` | `(WordChecks.url()`   |
| 19 | wordCheckIpv4          | ipv4检测策略(v0.25.0开始支持)                      | `WordChecks.ipv4()`   |
| 20 | wordCheckWord          | 敏感词检测策略(v0.25.0开始支持)                       | `WordChecks.word()`   |

内置实现：

a) `WordChecks.urlNoPrefix()` 作为 url 的额外实现，可以不需要 `https://` 和 `http://` 前缀。 

### 邮箱检测

邮箱等个人信息，默认未启用。

```java
final String text = "楼主好人，邮箱 sensitiveword@xx.com";
List<String> wordList = SensitiveWordBs.newInstance().enableEmailCheck(true).init().findAll(text);
Assert.assertEquals("[sensitiveword@xx.com]", wordList.toString());
```

### 连续数字检测

一般用于过滤手机号/QQ等广告信息，默认未启用。

V0.2.1 之后，支持通过 `numCheckLen(长度)` 自定义检测的长度。

```java
final String text = "你懂得：12345678";

// 默认检测 8 位
List<String> wordList = SensitiveWordBs.newInstance()
.enableNumCheck(true)
.init().findAll(text);
Assert.assertEquals("[12345678]", wordList.toString());

// 指定数字的长度，避免误杀
List<String> wordList2 = SensitiveWordBs.newInstance()
.enableNumCheck(true)
.numCheckLen(9)
.init()
.findAll(text);
Assert.assertEquals("[]", wordList2.toString());
```

### 网址检测

用于过滤常见的网址信息，默认未启用。

v0.18.0 优化 URL 检测，更加严格，降低误判率

```java
final String text = "点击链接 https://www.baidu.com 查看答案";
final SensitiveWordBs sensitiveWordBs = SensitiveWordBs.newInstance().enableUrlCheck(true).init();
List<String> wordList = sensitiveWordBs.findAll(text);
Assert.assertEquals("[https://www.baidu.com]", wordList.toString());
Assert.assertEquals("点击链接 ********************* 查看答案", sensitiveWordBs.replace(text));
```

v0.25.0 内置支持不需要 http 协议的前缀检测：

```java
final String text = "点击链接 https://www.baidu.com 查看答案，当然也可以是 baidu.com、www.baidu.com";

final SensitiveWordBs sensitiveWordBs = SensitiveWordBs.newInstance()
        .enableUrlCheck(true) // 启用URL检测
        .wordCheckUrl(WordChecks.urlNoPrefix()) //指定检测的方式
        .init();
List<String> wordList = sensitiveWordBs.findAll(text);
Assert.assertEquals("[www.baidu.com, baidu.com, www.baidu.com]", wordList.toString());

Assert.assertEquals("点击链接 https://************* 查看答案，当然也可以是 *********、*************", sensitiveWordBs.replace(text));
```

### IPV4 检测

v0.17.0 支持

避免用户通过 ip 绕过网址检测等，默认未启用。

```java
final String text = "个人网站，如果网址打不开可以访问 127.0.0.1。";
final SensitiveWordBs sensitiveWordBs = SensitiveWordBs.newInstance().enableIpv4Check(true).init();
List<String> wordList = sensitiveWordBs.findAll(text);
Assert.assertEquals("[127.0.0.1]", wordList.toString());
```

# 引导类特性配置

## 说明

上面的特性默认都是开启的，有时业务需要灵活定义相关的配置特性。

所以 v0.0.14 开放了属性配置。

## 配置方法

为了让使用更加优雅，统一使用 fluent-api 的方式定义。

用户可以使用 `SensitiveWordBs` 进行如下定义：

注意：配置后，要使用我们新定义的 `SensitiveWordBs` 的对象，而不是以前的工具方法。工具方法配置都是默认的。

```java
SensitiveWordBs wordBs = SensitiveWordBs.newInstance()
        .ignoreCase(true)
        .ignoreWidth(true)
        .ignoreNumStyle(true)
        .ignoreChineseStyle(true)
        .ignoreEnglishStyle(true)
        .ignoreRepeat(false)
        .enableNumCheck(false)
        .enableEmailCheck(false)
        .enableUrlCheck(false)
        .enableIpv4Check(false)
        .enableWordCheck(true)
        .wordFailFast(true)
        .wordCheckNum(WordChecks.num())
        .wordCheckEmail(WordChecks.email())
        .wordCheckUrl(WordChecks.url())
        .wordCheckIpv4(WordChecks.ipv4())
        .wordCheckWord(WordChecks.word())
        .numCheckLen(8)
        .wordTag(WordTags.none())
        .charIgnore(SensitiveWordCharIgnores.defaults())
        .wordResultCondition(WordResultConditions.alwaysTrue())
        .init();

final String text = "五星红旗迎风飘扬，毛主席的画像屹立在天安门前。";
Assert.assertTrue(wordBs.contains(text));
```
## 配置说明

其中各项配置的说明如下：

| 序号 | 方法                  | 说明                           | 默认值                       |
|:---|:--------------------|:-----------------------------|:--------------------------|
| 1  | ignoreCase          | 忽略大小写                        | true                      |
| 2  | ignoreWidth         | 忽略半角圆角                       | true                      |
| 3  | ignoreNumStyle      | 忽略数字的写法                      | true                      |
| 4  | ignoreChineseStyle  | 忽略中文的书写格式                    | true                      |
| 5  | ignoreEnglishStyle  | 忽略英文的书写格式                    | true                      |
| 6  | ignoreRepeat        | 忽略重复词                        | false                     |
| 7  | enableNumCheck      | 是否启用数字检测。                    | false                     |
| 8  | enableEmailCheck    | 是有启用邮箱检测                     | false                     |
| 9  | enableUrlCheck      | 是否启用链接检测                     | false                     |
| 10 | enableIpv4Check     | 是否启用IPv4检测                   | false                     |
| 11 | enableWordCheck     | 是否启用敏感单词检测                   | true                      |
| 12 | numCheckLen         | 数字检测，自定义指定长度。                | 8                         |
| 13 | wordTag             | 词对应的标签                       | none                      |
| 14 | charIgnore          | 忽略的字符                        | none                      |
| 15 | wordResultCondition | 针对匹配的敏感词额外加工，比如可以限制英文单词必须全匹配 | 恒为真                       |
| 16 | wordCheckNum        | 数字检测策略(v0.25.0开始支持)          | `WordChecks.num()`        |
| 17 | wordCheckEmail      | 邮箱检测策略(v0.25.0开始支持)          | `WordChecks.email()`      |
| 18 | wordCheckUrl        | URL检测策略(v0.25.0开始支持)         | `(WordChecks.url()`       |
| 19 | wordCheckIpv4       | ipv4检测策略(v0.25.0开始支持)        | `WordChecks.ipv4()`       |
| 20 | wordCheckWord       | 敏感词检测策略(v0.25.0开始支持)         | `WordChecks.word()`       |
| 21 | wordReplace         | 替换策略                         | `WordReplaces.defaults()` |
| 22 | wordFailFast        | 敏感词匹配模式是否快速返回                | true                      |


## wordFailFast 敏感词匹配快速失败模式

### 场景说明

v0.26.0 开始支持。

默认情况下，wordFailFast=true。匹配时快速返回，性能较好。

但是有时候不太符合人的直觉。

默认如下：

```java
SensitiveWordBs bs2 = SensitiveWordBs.newInstance()
        .wordDeny(new IWordDeny() {
            @Override
            public List<String> deny() {
                return Arrays.asList("我的世界", "我的");
            }
        }).init();
String text = "他的世界它的世界和她的世界都不是我的也不是我的世界";
List<String> textList2 = bs2.findAll(text);
Assert.assertEquals(Arrays.asList("我的", "我的"), textList2);
```

此时会优先匹配短的【我的】，导致后面的【我的世界】被跳过。

### failOver 模式

尽可能找到最长的匹配词。

```java
SensitiveWordBs bs = SensitiveWordBs.newInstance()
        .wordFailFast(false)
        .wordDeny(new IWordDeny() {
            @Override
            public List<String> deny() {
                return Arrays.asList("我的世界", "我的");
            }
        }).init();

String text = "他的世界它的世界和她的世界都不是我的也不是我的世界";
List<String> textList = bs.findAll(text);
Assert.assertEquals(Arrays.asList("我的", "我的世界"), textList);
```

## 内存资源的释放

v0.16.1 开始支持，有时候我们需要释放内存，可以如下：

> [关于内存回收问题](https://github.com/houbb/sensitive-word/issues/53)

```java
SensitiveWordBs wordBs = SensitiveWordBs.newInstance()
                .init();
// 后续因为一些原因移除了对应信息，希望释放内存。
wordBs.destroy();
```

## 针对单个黑名单词的新增/删除，无需全量初始化

使用场景：在初始化之后，我们希望针对单个词的新增/删除，而不是完全重新初始化。这个特性就是为此准备的。

支持版本：v0.19.0

### 方法说明 

`addWord(word)` 新增敏感词，支持单个词/集合

`removeWord(word)` 删除敏感词，支持单个词/集合

### 实例代码：

```java
final String text = "测试一下新增敏感词，验证一下删除和新增对不对";

SensitiveWordBs sensitiveWordBs =
SensitiveWordBs.newInstance()
        .wordAllow(WordAllows.empty())
        .wordDeny(WordDenys.empty())
        .init();

// 当前
Assert.assertEquals("[]", sensitiveWordBs.findAll(text).toString());

// 新增单个
sensitiveWordBs.addWord("测试");
sensitiveWordBs.addWord("新增");
Assert.assertEquals("[测试, 新增, 新增]", sensitiveWordBs.findAll(text).toString());

// 删除单个
sensitiveWordBs.removeWord("新增");
Assert.assertEquals("[测试]", sensitiveWordBs.findAll(text).toString());
sensitiveWordBs.removeWord("测试");
Assert.assertEquals("[]", sensitiveWordBs.findAll(text).toString());

// 新增集合
sensitiveWordBs.addWord(Arrays.asList("新增", "测试"));
Assert.assertEquals("[测试, 新增, 新增]", sensitiveWordBs.findAll(text).toString());
// 删除集合
sensitiveWordBs.removeWord(Arrays.asList("新增", "测试"));
Assert.assertEquals("[]", sensitiveWordBs.findAll(text).toString());

// 新增数组
sensitiveWordBs.addWord("新增", "测试");
Assert.assertEquals("[测试, 新增, 新增]", sensitiveWordBs.findAll(text).toString());
// 删除集合
sensitiveWordBs.removeWord("新增", "测试");
Assert.assertEquals("[]", sensitiveWordBs.findAll(text).toString());
```

## 针对单个白名单词的新增/删除，无需全量初始化

使用场景：在初始化之后，我们希望针对单个词的新增/删除，而不是完全重新初始化。这个特性就是为此准备的。

支持版本：v0.21.0

### 方法说明

`addWordAllow(word)` 新增白名单，支持单个词/集合

`removeWordAllow(word)` 删除白名单，支持单个词/集合

### 使用例子

```java
        final String text = "测试一下新增敏感词白名单，验证一下删除和新增对不对";

        SensitiveWordBs sensitiveWordBs =
                SensitiveWordBs.newInstance()
                        .wordAllow(WordAllows.empty())
                        .wordDeny(new IWordDeny() {
                            @Override
                            public List<String> deny() {
                                return Arrays.asList("测试", "新增");
                            }
                        })
                        .init();

        // 当前
        Assert.assertEquals("[测试, 新增, 新增]", sensitiveWordBs.findAll(text).toString());

        // 新增单个
        sensitiveWordBs.addWordAllow("测试");
        sensitiveWordBs.addWordAllow("新增");
        Assert.assertEquals("[]", sensitiveWordBs.findAll(text).toString());

        // 删除单个
        sensitiveWordBs.removeWordAllow("测试");
        Assert.assertEquals("[测试]", sensitiveWordBs.findAll(text).toString());
        sensitiveWordBs.removeWordAllow("新增");
        Assert.assertEquals("[测试, 新增, 新增]", sensitiveWordBs.findAll(text).toString());

        // 新增集合
        sensitiveWordBs.addWordAllow(Arrays.asList("新增", "测试"));
        Assert.assertEquals("[]", sensitiveWordBs.findAll(text).toString());
        // 删除集合
        sensitiveWordBs.removeWordAllow(Arrays.asList("新增", "测试"));
        Assert.assertEquals("[测试, 新增, 新增]", sensitiveWordBs.findAll(text).toString());

        // 新增数组
        sensitiveWordBs.addWordAllow("新增", "测试");
        Assert.assertEquals("[]", sensitiveWordBs.findAll(text).toString());
        // 删除集合
        sensitiveWordBs.removeWordAllow("新增", "测试");
        Assert.assertEquals("[测试, 新增, 新增]", sensitiveWordBs.findAll(text).toString());
```

## 全量初始化

### 说明

此方式**已废弃**，建议使用上面增量添加的方式，避免全量加载。为了兼容，此方式依然保留。

使用方式：在调用 `sensitiveWordBs.init()` 的时候，根据 IWordDeny+IWordAllow 重新构建敏感词库。 因为初始化可能耗时较长（秒级别），所有优化为 init 未完成时**不影响旧的词库功能，完成后以新的为准**。

### 例子

```java
@Component
public class SensitiveWordService {

    @Autowired
    private SensitiveWordBs sensitiveWordBs;

    /**
     * 更新词库
     *
     * 每次数据库的信息发生变化之后，首先调用更新数据库敏感词库的方法。
     * 如果需要生效，则调用这个方法。
     *
     * 说明：重新初始化不影响旧的方法使用。初始化完成后，会以新的为准。
     */
    public void refresh() {
        // 每次数据库的信息发生变化之后，首先调用更新数据库敏感词库的方法，然后调用这个方法。
        sensitiveWordBs.init();
    }

}
```

如上，你可以在数据库词库发生变更时，需要词库生效，主动触发一次初始化 `sensitiveWordBs.init();`。

其他使用保持不变，无需重启应用。

# wordResultCondition-针对匹配词进一步判断

## 说明

支持版本：v0.13.0

有时候我们可能希望对匹配的敏感词进一步限制，比如虽然我们定义了【av】作为敏感词，但是不希望【have】被匹配。

就可以自定义实现 wordResultCondition 接口，实现自己的策略。

系统内置的策略在 `WordResultConditions#alwaysTrue()` 恒为真，`WordResultConditions#englishWordMatch()` 则要求英文必须全词匹配。

## 内置策略

WordResultConditions 工具类可以获取匹配策略

| 实现                                         | 说明                  | 支持版本    |
|:-------------------------------------------|:--------------------|:--------|
| alwaysTrue                                 | 恒为真                 |         |
| englishWordMatch                           | 英文单词全词匹配            | v0.13.0 |
| englishWordNumMatch                        | 英文单词/数字全词匹配         | v0.20.0 |
| wordTags                                   | 满足特定标签的，比如只关注【广告】标签 | v0.23.0 |
| chains(IWordResultCondition ...conditions) | 支持指定多个条件，同时满足       | v0.23.0 |

## 使用例子

原始的默认情况：

```java
final String text = "I have a nice day。";

List<String> wordList = SensitiveWordBs.newInstance()
        .wordDeny(new IWordDeny() {
            @Override
            public List<String> deny() {
                return Collections.singletonList("av");
            }
        })
        .wordResultCondition(WordResultConditions.alwaysTrue())
        .init()
        .findAll(text);
Assert.assertEquals("[av]", wordList.toString());
```

我们可以指定为英文必须全词匹配。

```java
final String text = "I have a nice day。";

List<String> wordList = SensitiveWordBs.newInstance()
        .wordDeny(new IWordDeny() {
            @Override
            public List<String> deny() {
                return Collections.singletonList("av");
            }
        })
        .wordResultCondition(WordResultConditions.englishWordMatch())
        .init()
        .findAll(text);
Assert.assertEquals("[]", wordList.toString());
```

当然可以根据需要实现更加复杂的策略。

## wordTags 单词标签

支持版本： `v0.23.0`

我们可以只返回隶属于某一种标签的敏感词。

我们指定了两个敏感词：商品、AV

MyWordTag 是我们定义的一个敏感词标签实现：

```java
/**
 * 自定义单词标签
 * @since 0.23.0
 */
public class MyWordTag extends AbstractWordTag {

    private static Map<String, Set<String>> dataMap;

    static {
        dataMap = new HashMap<>();
        dataMap.put("商品", buildSet("广告", "中文"));
        dataMap.put("AV", buildSet("色情", "单词", "英文"));
    }

    private static Set<String> buildSet(String... tags) {
        Set<String> set = new HashSet<>();
        for(String tag : tags) {
            set.add(tag);
        }
        return set;
    }

    @Override
    protected Set<String> doGetTag(String word) {
        return dataMap.get(word);
    }

}
```

测试用例如下，我们模拟了两个不同的实现类，每一个关注的单词标签不同。

```java
// 只关心SE情
SensitiveWordBs sensitiveWordBsYellow = SensitiveWordBs.newInstance()
        .wordDeny(new IWordDeny() {
            @Override
            public List<String> deny() {
                return Arrays.asList("商品", "AV");
            }
        })
        .wordAllow(WordAllows.empty())
        .wordTag(new MyWordTag())
        .wordResultCondition(WordResultConditions.wordTags(Arrays.asList("色情")))
        .init();

// 只关心广告
SensitiveWordBs sensitiveWordBsAd = SensitiveWordBs.newInstance()
        .wordDeny(new IWordDeny() {
            @Override
            public List<String> deny() {
                return Arrays.asList("商品", "AV");
            }
        })
        .wordAllow(WordAllows.empty())
        .wordTag(new MyWordTag())
        .wordResultCondition(WordResultConditions.wordTags(Arrays.asList("广告")))
        .init();

final String text = "这些 AV 商品什么价格？";
Assert.assertEquals("[AV]", sensitiveWordBsYellow.findAll(text).toString());
Assert.assertEquals("[商品]", sensitiveWordBsAd.findAll(text).toString());
```

# 忽略字符

## 说明

我们的敏感词一般都是比较连续的，比如【傻帽】

那就有大聪明发现，可以在中间加一些字符，比如【傻!@#$帽】跳过检测，但是骂人等攻击力不减。

那么，如何应对这些类似的场景呢？

我们可以指定特殊字符的跳过集合，忽略掉这些无意义的字符即可。

v0.11.0 开始支持

## 例子

其中 charIgnore 对应的字符策略，用户可以自行灵活定义。

```java
final String text = "傻@冒，狗+东西";

//默认因为有特殊字符分割，无法识别
List<String> wordList = SensitiveWordBs.newInstance().init().findAll(text);
Assert.assertEquals("[]", wordList.toString());

// 指定忽略的字符策略，可自行实现。
List<String> wordList2 = SensitiveWordBs.newInstance()
        .charIgnore(SensitiveWordCharIgnores.specialChars())
        .init()
        .findAll(text);

Assert.assertEquals("[傻@冒, 狗+东西]", wordList2.toString());
```

# 敏感词标签

## 说明

有时候我们希望对敏感词加一个分类标签：比如社情、暴/力等等。

这样后续可以按照标签等进行更多特性操作，比如只处理某一类的标签。

支持版本：v0.10.0

主要特性支持版本：v0.24.0

## 标签接口

这里只是一个抽象的接口，用户可以自行定义实现。比如从数据库查询、文件读取、api 调用等。

```java
public interface IWordTag {

    /**
     * 查询标签列表
     * @param word 脏词
     * @return 结果
     */
    Set<String> getTag(String word);

}
```

## 内置实现

### 方法列表

为了方便大部分情况使用，内置实现一些场景策略在 `WordTags` 类中

| 实现方法                                                              | 说明                   | 备注         |
|:------------------------------------------------------------------|:---------------------|:-----------|
| none()                                                            | 空实现                  | v0.10.0 支持 |
| file(String filePath)                                             | 指定文件路径               | v0.10.0 支持 |
| file(String filePath, String wordSplit, String tagSplit)          | 指定文件路径，以及单词分隔符、标签分隔符 | v0.10.0 支持 |
| map(final Map<String, Set<String>> wordTagMap)                    | 根据 map初始化            | v0.24.0 支持 |
| lines(Collection<String> lines)                                   | 字符串列表                | v0.24.0 支持 |
| lines(Collection<String> lines, String wordSplit, String tagSpli) | 字符串列表，以及单词分隔符、标签分隔符  | v0.24.0 支持 |
| system()                                                          | 系件文件内置实现，整合网络分类      | v0.24.0 支持 |
| defaults()                                                        | 默认策略，目前为 system      | v0.24.0 支持 |
| chains(IWordTag... others)                 | 链式方法，支持用户整合实现多个策略    | v0.24.0 支持 |

### 格式约定

敏感词标签的格式我们默认约定如下 `敏感词 tag1,tag2`，代表这 `敏感词` 的标签为 tag1 和 tag2

比如 

```
五星红旗 政治,国家
```

所有的文件行内容，和指定的字符串行内容也建议用这种方式。如果不满足，自定义实现即可。

## 系统内置实现（默认效果）

v0.24.0 版本开始，默认的单词标签为 `WordTags.system()`。

说明：目前数据统计自网络，存在不少疏漏。也欢迎大家指正，持续改进中...

```java
SensitiveWordBs sensitiveWordBs = SensitiveWordBs.newInstance()
.wordTag(WordTags.system())
.init();
Set<String> tagSet = sensitiveWordBs.tags("博彩");
Assert.assertEquals("[3]", tagSet.toString());
```

这里为了压缩大小优化，对应的类别用数字表示。

数字的含义列表如下：

```
0 政治
1 毒品
2 色情
3 赌博
4 违法
```

## 文件入门例子

这里以文件为例子，演示一下如何使用。

```java
final String path = "~\\test\\resources\\dict_tag_test.txt";

// 演示默认方法
IWordTag wordTag = WordTags.file(path);
SensitiveWordBs sensitiveWordBs = SensitiveWordBs.newInstance()
        .wordTag(wordTag)
        .init();

Set<String> tagSet = sensitiveWordBs.tags("零售");
        Assert.assertEquals("[广告, 网络]", tagSet.toString());


// 演示指定分隔符
IWordTag wordTag2 = WordTags.file(path, " ", ",");
SensitiveWordBs sensitiveWordBs2 = SensitiveWordBs.newInstance()
        .wordTag(wordTag2)
        .init();
Set<String> tagSet2 = sensitiveWordBs2.tags("零售");
        Assert.assertEquals("[广告, 网络]", tagSet2.toString());
```

其中 `dict_tag_test.txt` 我们自定义的内容如下：

```
零售 广告,网络
```

## 单词标签和敏感词发现的联动

我们在获取敏感词的时候，是可以设置对应的结果处理策略，从而获取对应的敏感词标签信息

```java
// 自定义测试标签类
IWordTag wordTag = WordTags.lines(Arrays.asList("天安门 政治,国家,地址"));

// 指定初始化
SensitiveWordBs sensitiveWordBs = SensitiveWordBs.newInstance()
        .wordTag(wordTag)
        .init()
        ;

List<WordTagsDto> wordTagsDtoList1 = sensitiveWordBs.findAll("天安门", WordResultHandlers.wordTags());
Assert.assertEquals("[WordTagsDto{word='天安门', tags=[政治, 国家, 地址]}]", wordTagsDtoList1.toString());
```

我们自定义了 `天安门` 关键词的标签，然后通过指定 findAll 的结果处理策略为 `WordResultHandlers.wordTags()`，就可以在获取敏感词的同时，获取对应的标签列表。

# 动态加载（用户自定义）

## 情景说明

有时候我们希望将敏感词的加载设计成动态的，比如控台修改，然后可以实时生效。

v0.0.13 支持了这种特性。

## 接口说明

为了实现这个特性，并且兼容以前的功能，我们定义了两个接口。

### IWordDeny

接口如下，可以自定义自己的实现。

返回的列表，表示这个词是一个敏感词。

```java
/**
 * 拒绝出现的数据-返回的内容被当做是敏感词
 * @author binbin.hou
 * @since 0.0.13
 */
public interface IWordDeny {

    /**
     * 获取结果
     * @return 结果
     * @since 0.0.13
     */
    List<String> deny();

}
```

比如：

```java
public class MyWordDeny implements IWordDeny {

    @Override
    public List<String> deny() {
        return Arrays.asList("我的自定义敏感词");
    }

}
```

### IWordAllow

接口如下，可以自定义自己的实现。

返回的列表，表示这个词不是一个敏感词。

```java
/**
 * 允许的内容-返回的内容不被当做敏感词
 * @author binbin.hou
 * @since 0.0.13
 */
public interface IWordAllow {

    /**
     * 获取结果
     * @return 结果
     * @since 0.0.13
     */
    List<String> allow();

}
```

如：

```java
public class MyWordAllow implements IWordAllow {

    @Override
    public List<String> allow() {
        return Arrays.asList("五星红旗");
    }

}
```

## 配置使用

**接口自定义之后，当然需要指定才能生效。**

为了让使用更加优雅，我们设计了引导类 `SensitiveWordBs`。

可以通过 wordDeny() 指定敏感词，wordAllow() 指定非敏感词，通过 init() 初始化敏感词字典。

### 系统的默认配置

```java
SensitiveWordBs wordBs = SensitiveWordBs.newInstance()
        .wordDeny(WordDenys.defaults())
        .wordAllow(WordAllows.defaults())
        .init();

final String text = "五星红旗迎风飘扬，毛主席的画像屹立在天安门前。";
Assert.assertTrue(wordBs.contains(text));
```

备注：init() 对于敏感词 DFA 的构建是比较耗时的，一般建议在应用初始化的时候**只初始化一次**。而不是重复初始化！

### 指定自己的实现

我们可以测试一下自定义的实现，如下:

```java
String text = "这是一个测试，我的自定义敏感词。";

SensitiveWordBs wordBs = SensitiveWordBs.newInstance()
        .wordDeny(new MyWordDeny())
        .wordAllow(new MyWordAllow())
        .init();

Assert.assertEquals("[我的自定义敏感词]", wordBs.findAll(text).toString());
```

这里只有 `我的自定义敏感词` 是敏感词，而 `测试` 不是敏感词。

当然，这里是全部使用我们自定义的实现，一般建议使用系统的默认配置+自定义配置。

可以使用下面的方式。

### 同时配置多个

- 多个敏感词

`WordDenys.chains()` 方法，将多个实现合并为同一个 IWordDeny。

- 多个白名单

`WordAllows.chains()` 方法，将多个实现合并为同一个 IWordAllow。

例子：

```java
String text = "这是一个测试。我的自定义敏感词。";

IWordDeny wordDeny = WordDenys.chains(WordDenys.defaults(), new MyWordDeny());
IWordAllow wordAllow = WordAllows.chains(WordAllows.defaults(), new MyWordAllow());

SensitiveWordBs wordBs = SensitiveWordBs.newInstance()
        .wordDeny(wordDeny)
        .wordAllow(wordAllow)
        .init();

Assert.assertEquals("[我的自定义敏感词]", wordBs.findAll(text).toString());
```

这里都是同时使用了系统默认配置，和自定义的配置。

注意：**我们初始化了新的 wordBs，那么用新的 wordBs 去判断。而不是用以前的 `SensitiveWordHelper` 工具方法，工具方法配置是默认的！**


# 系统内置词库及如何排除

## 内置词库文件说明

v0.27.0 将词库和当前项目拆分开，词库可以在 [https://github.com/houbb/sensitive-word-data](https://github.com/houbb/sensitive-word-data) 项目查看。

对应的资源文件在 [https://github.com/houbb/sensitive-word-data/tree/main/src/main/resources](https://github.com/houbb/sensitive-word-data/tree/main/src/main/resources) 目录下

| 文件                           | 说明         | 默认加载类              
|:-----------------------------|:-----------|:-------------------|
| `sensitive_word_allow.txt`   | 内置自定义白名单词库 | `WordAllowSystem`  |
| `sensitive_word_deny.txt`    | 内置自定义黑名单词库 |  `WordDenySystem`                  |
| `sensitive_word_dict.txt`    | 内置黑名单词库    |   `WordDenySystem`                 |
| `sensitive_word_dict_en.txt` | 内置黑名单英文词库  |   `WordDenySystem`                 |
| `sensitive_word_tags.txt`    | 内置敏感词标签词库  |   `WordTagSystem`                 |

## 如何排除

比如一些 android app 引入时不希望包中内置敏感的信息，希望对词库加解密或者是放在服务端初始化加载。

系统的内置词库通过下面的 maven 依赖导入

```xml
<dependency>
    <groupId>com.github.houbb</groupId>
    <artifactId>sensitive-word-data</artifactId>
    <version>${sensitive-word-data.version}</version>
</dependency>
```

### 依赖排除

所以可以按照 maven 排除规范，如下将其排除

```xml
<dependency>
    <groupId>com.github.houbb</groupId>
    <artifactId>sensitive-word</artifactId>
    <version>${sensitive-word.version}</version>
    <exclusions>
        <exclusion>
            <groupId>com.github.houbb</groupId>
            <artifactId>sensitive-word-data</artifactId>
        </exclusion>
    </exclusions>
</dependency>
```

## 排除后自定义

不希望使用内置词库，那就需要将原来内置的词库依赖改为自己的依赖

默认配置项：

```java
SensitiveWordBs sensitiveWordBs = SensitiveWordBs.newInstance()
                .wordAllow(WordAllows.defaults())
                .wordDeny(WordDenys.defaults())
                .wordTag(WordTags.defaults())
                .init();
```

你可以将用到的这3个类，改为自己的实现。

可以通过加解密，或者加载远程服务的文件信息都可以。

# spring 整合

## 背景

实际使用中，比如可以在页面配置修改，然后实时生效。

数据存储在数据库中，下面是一个伪代码的例子，可以参考 [SpringSensitiveWordConfig.java](https://github.com/houbb/sensitive-word/blob/master/src/test/java/com/github/houbb/sensitive/word/spring/SpringSensitiveWordConfig.java)

要求，版本 v0.0.15 及其以上。

## 自定义数据源

简化伪代码如下，数据的源头为数据库。

MyDdWordAllow 和 MyDdWordDeny 是基于数据库为源头的自定义实现类。

```java
@Configuration
public class SpringSensitiveWordConfig {

    @Autowired
    private MyDdWordAllow myDdWordAllow;

    @Autowired
    private MyDdWordDeny myDdWordDeny;

    /**
     * 初始化引导类
     * @return 初始化引导类
     * @since 1.0.0
     */
    @Bean
    public SensitiveWordBs sensitiveWordBs() {
        SensitiveWordBs sensitiveWordBs = SensitiveWordBs.newInstance()
                .wordAllow(WordAllows.chains(WordAllows.defaults(), myDdWordAllow))
                .wordDeny(myDdWordDeny)
                // 各种其他配置
                .init();

        return sensitiveWordBs;
    }

}
```

敏感词库的初始化较为耗时，建议程序启动时做一次 init 初始化。

# Benchmark

V0.6.0 以后，添加对应的 benchmark 测试。

> [BenchmarkTimesTest](https://github.com/houbb/sensitive-word/blob/master/src/test/java/com/github/houbb/sensitive/word/benchmark/BenchmarkTimesTest.java)

## 环境

测试环境为普通的笔记本:

```
处理器	12th Gen Intel(R) Core(TM) i7-1260P   2.10 GHz
机带 RAM	16.0 GB (15.7 GB 可用)
系统类型	64 位操作系统, 基于 x64 的处理器
```

ps: 不同环境会有差异，但是比例基本稳定。

## 测试效果记录

测试数据：100+ 字符串，循环 10W 次。

| 序号 | 场景               | 耗时 | 备注            |
|:----|:-----------------|:----|:--------------|
| 1 | 只做敏感词，无任何格式转换    | 1470ms，约 7.2W QPS | 追求极致性能，可以这样配置 |
| 2 | 只做敏感词，支持全部格式转换  | 2744ms，约 3.7W QPS | 满足大部分场景       |

# STAR

[![Stargazers over time](https://starchart.cc/houbb/sensitive-word.svg)](https://starchart.cc/houbb/sensitive-word)

# 后期 road-map

- [x] 移除单个汉字的敏感词，在中国，要把词组当做一次词，降低误判率。

- [x] 支持单个的敏感词变化？

remove、add、edit?

- [x] 敏感词标签接口支持

- [x] 敏感词处理时标签支持

- [x] wordData 的内存占用对比 + 优化

- [x] 用户指定自定义的词组，同时允许指定词组的组合获取，更加灵活

FormatCombine/CheckCombine/AllowDenyCombine 组合策略，允许用户自定义。

- [ ] word check 策略的优化，统一遍历+转换

- [ ] 添加 ThreadLocal 等性能优化

# 拓展阅读

# 敏感词系列

[sensitive-word-admin 敏感词控台 v1.2.0 版本开源](https://mp.weixin.qq.com/s/7wSy0PuJLTudEo9gTY5s5w)

[sensitive-word-admin v1.3.0 发布 如何支持分布式部署？](https://mp.weixin.qq.com/s/4wia8SlQQbLV5_OHplaWvg)

[01-开源敏感词工具入门使用](https://houbb.github.io/2020/01/07/sensitive-word-00-overview)

[02-如何实现一个敏感词工具？违禁词实现思路梳理](https://houbb.github.io/2020/01/07/sensitive-word-01-intro)

[03-敏感词之 StopWord 停止词优化与特殊符号](https://houbb.github.io/2020/01/07/sensitive-word-02-stopword)

[04-敏感词之字典瘦身](https://houbb.github.io/2020/01/07/sensitive-word-03-slim)

[05-敏感词之 DFA 算法(Trie Tree 算法)详解](https://houbb.github.io/2020/01/07/sensitive-word-04-dfa)

[06-敏感词(脏词) 如何忽略无意义的字符？达到更好的过滤效果](https://houbb.github.io/2020/01/07/sensitive-word-05-ignore-char)

[v0.10.0-脏词分类标签初步支持](https://juejin.cn/post/7308782855941292058?searchId=20231209140414C082B3CCF1E7B2316EF9)

[v0.11.0-敏感词新特性：忽略无意义的字符，词标签字典](https://mp.weixin.qq.com/s/m40ZnR6YF6WgPrArUSZ_0g)

[v0.12.0-敏感词/脏词词标签能力进一步增强](https://mp.weixin.qq.com/s/-wa-if7uAy2jWsZC13C0cQ)

[v0.13.0-敏感词特性版本发布 支持英文单词全词匹配](https://mp.weixin.qq.com/s/DXv5OUyOs0y2dAq8nFWJ9A)

[v0.16.1-敏感词新特性之字典内存资源释放](https://mp.weixin.qq.com/s/zbeJR-OkWjxashtjiopnMA)

[v0.19.0-敏感词新特性之敏感词单个编辑，不必重复初始化](https://houbb.github.io/2020/01/07/sensitive-word-10-v0.19.0-deny-word-edit)

[v0.20.0 敏感词新特性之数字全部匹配，而不是部分匹配](https://houbb.github.io/2020/01/07/sensitive-word-11-v0.20.0-num-match)

[v0.21.0 敏感词新特性之白名单支持单个编辑，修正白名单包含黑名单时的问题](https://houbb.github.io/2020/01/07/sensitive-word-12-v0.21.0-allow-word-edit)

[v0.23.0 敏感词结果条件拓展，内置支持链式+单词标签](https://houbb.github.io/2020/01/07/sensitive-word-13-v0.23.0-result-condition-enhance)

[v0.24.0 新特性支持标签分类，内置实现多种策略](https://houbb.github.io/2020/01/07/sensitive-word-13-v0.24.0-word-tag-impl)

[v0.25.0 新特性之 wordCheck 策略支持用户自定义](https://houbb.github.io/2020/01/07/sensitive-word-14-v0.25.0-url-define)

[v0.25.1 新特性之返回匹配词，修正 tags 标签](https://houbb.github.io/2020/01/07/sensitive-word-14-v0.25.1-tags-match)

[v0.27.0 敏感词库独立拆分](https://houbb.github.io/2020/01/07/sensitive-word-15-v0.27.0-dict-split)

![wechat](https://img-blog.csdnimg.cn/63926529df364f09bcb203a8a9016854.png)

# NLP 开源矩阵

[pinyin 汉字转拼音](https://github.com/houbb/pinyin)

[pinyin2hanzi 拼音转汉字](https://github.com/houbb/pinyin2hanzi)

[segment 高性能中文分词](https://github.com/houbb/segment)

[opencc4j 中文繁简体转换](https://github.com/houbb/opencc4j)

[nlp-hanzi-similar 汉字相似度](https://github.com/houbb/nlp-hanzi-similar)

[word-checker 拼写检测](https://github.com/houbb/word-checker)

[sensitive-word 敏感词](https://github.com/houbb/sensitive-word)

