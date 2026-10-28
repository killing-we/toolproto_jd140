# toolproto_jd140

**在工具调用协议工程师·查询改写的语义漂移里找出重复内容并给出归并建议。**

`toolproto_jd140` —— 对内容做归一化与分片比对，找出工具调用协议工程师·查询改写的语义漂移上的重复项并按相似度归并

- 零依赖，Python 3.10+ 标准库即可运行
- 单文件，`toolproto_jd140.py` 拷走就能用
- 不联网、不写文件

## 对应的岗位

- 目标岗位：**美团 · 资深工具调用协议工程师**
- 技能主线：Agent、Prompt工程、Python
- 领域标签：大模型应用、NLP
- 研究方向：工具调用协议工程师·查询改写的语义漂移

工具里的规则表就是照着上面这条岗位要求建的——每条规则都挂在技能线或领域标签上，命中时能指回具体要求。

<!-- ipos:install -->
## 安装

零依赖，Python 3.10+ 即可：

```bash
pip install killing-we-toolproto_jd140
```

装完直接用命令名调用：

```bash
toolproto_jd140 --help
```

也可以不用安装，直接把 `toolproto_jd140.py` 拷走用——它只依赖标准库。

## 为什么需要它

按归一化后的分片相似度判断，而不是按字符串完全相等

它遵守下面几条自己定的规矩：

1. **只报告能定位到具体位置的结论**，不做语义猜测。
2. **规则表公开**，每条命中都能对应到岗位要求的一条明示规则。
3. **输入为空或格式不对时明确报错**，不静默返回空结果。

## 用法

```bash
python toolproto_jd140.py --file input.txt
python toolproto_jd140.py --text "示例内容"
python toolproto_jd140.py --file input.txt --json
```

加 `--json` 可以拿到机器可读的结果，便于接到流水线里。

## 已知局限

- 近重复用字符 shingle 估算，长文本阈值需自己调。
- 只报告重复项，不删数据。

## 跑测试

```bash
python test_toolproto_jd140.py
```

测试用独立的断言与临时数据，不污染工作目录。

## 来源与参考

- Python 标准库文档：<https://docs.python.org/3/>
- GitHub 仓库：<https://github.com/killing-we/toolproto_jd140>

---

## 关于作者

killing-we 做工具调用协议工程师·查询改写的语义漂移相关的问题，方向对标美团的资深工具调用协议工程师岗位。这个工具先替你回答一个具体问题，再谈别的。

- 个人主页：<https://killing-we.github.io>
- 仓库：<https://github.com/killing-we/toolproto_jd140>

## 许可

MIT，见 [LICENSE](LICENSE)。
