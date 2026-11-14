# X（推特）数据接口（X / Twitter API）：帖子搜索、帖子详情、账号、粉丝、趋势、社群

**推特数据 API · X 帖子搜索 · 推文详情和回复 · 推特账号和粉丝 · X 趋势 · X 列表和社群。**

这个仓库是 [okdata](https://okdata.online/zh/?src=gh-x-twitter-api) 的X（推特）接口示例：20 个接口在线可用，一个 API Key 调用，按次计费（$0.0001 起），失败不扣费。不用登录平台账号，不用 Cookie，不开浏览器，所以也不存在账号被风控的问题。

[免费注册拿 Key（送 $0.1 试用额度）](https://okdata.online/zh/signup/?src=gh-x-twitter-api) · [全部接口文档](https://okdata.online/zh/apis/?src=gh-x-twitter-api) · [接入 AI（MCP）](https://okdata.online/zh/mcp/?src=gh-x-twitter-api)

## 接口清单

| 接口 | 说明 | 价格 | 路径 |
|---|---|---|---|
| [X 帖子详情](https://okdata.online/zh/apis/x/posts/get/) | 按 ID 或链接取一条帖子：正文、媒体、浏览、点赞、转发和回复。 | $0.0003 / 次 | `GET /v1/x/posts/get` |
| [X 帖子搜索](https://okdata.online/zh/apis/x/posts/search/) | 按查询词搜帖子（支持 X 的搜索语法），可按最新或热门。 | $0.002 / 次 | `GET /v1/x/posts/search` |
| [X 账号信息](https://okdata.online/zh/apis/x/users/get/) | 按用户名或数字 ID 取一个账号，或一次按 ID 取最多 100 个：粉丝、关注、发帖数、简介和认证。没找到的 ID 列在 data.missing 里，不收费。 | 每条 $0.0004（最少 $0.0004） | `GET /v1/x/users/get` |
| [X 账号帖子列表](https://okdata.online/zh/apis/x/users/posts/list/) | 账号发布的帖子，从新到旧。 | $0.002 / 次 | `GET /v1/x/users/posts/list` |
| [X 趋势](https://okdata.online/zh/apis/x/trends/list/) | 全球或某个国家的趋势话题。 | $0.009 / 次 | `GET /v1/x/trends/list` |
| [X 帖子回复](https://okdata.online/zh/apis/x/posts/replies/list/) | 一条帖子下面的回复，按 X 自己的相关度排，每页最多约 60 条。X 的回复本身就是帖子，所以按帖子返回：正文、作者、发布时间、浏览、点赞和它自己的回复数。 | $0.002 / 次 | `GET /v1/x/posts/replies/list` |
| [X 帖子引用](https://okdata.online/zh/apis/x/posts/quotes/list/) | 引用了某条帖子的帖子，按最新或最热排，每页 20 条：别人加了什么话、是谁、传播得怎样。 | 每条 $0.0003（最少 $0.0003） | `GET /v1/x/posts/quotes/list` |
| [X 帖子转推用户](https://okdata.online/zh/apis/x/posts/retweeters/list/) | 转推了某条帖子的账号，每页约 100 个：用户名、名称、简介和粉丝数。 | $0.002 / 次 | `GET /v1/x/posts/retweeters/list` |
| [X 长文](https://okdata.online/zh/apis/x/posts/article/get/) | 按帖子 ID 取它所附的 X 长文（Article）：标题、全文、作者、发布时间、浏览、点赞和回复。 | $0.002 / 次 | `GET /v1/x/posts/article/get` |
| [X 对话串](https://okdata.online/zh/apis/x/threads/posts/list/) | 给对话串里任意一条帖子的 ID，取整串帖子：起头的主帖、作者的续帖和其间的回复。每页多少由 X 决定，最多约 50 条。 | 每条 $0.0003（最少 $0.0003） | `GET /v1/x/threads/posts/list` |
| [X 账号搜索](https://okdata.online/zh/apis/x/users/search/) | 按关键词找账号，每页 20 个：用户名、名称、简介、粉丝、关注、发帖数和认证。 | 每条 $0.0004（最少 $0.0004） | `GET /v1/x/users/search` |
| [X 账号粉丝](https://okdata.online/zh/apis/x/users/followers/list/) | 关注了某个账号的人，最新关注的在前，每页 200 个：用户名、名称、简介、粉丝数和发帖数。 | 每条 $0.0001（最少 $0.0004） | `GET /v1/x/users/followers/list` |
| [X 账号关注](https://okdata.online/zh/apis/x/users/following/list/) | 某个账号关注的人，最近关注的在前，每页 200 个：用户名、名称、简介、粉丝数和发帖数。 | 每条 $0.0001（最少 $0.0004） | `GET /v1/x/users/following/list` |
| [X 账号被提及](https://okdata.online/zh/apis/x/users/mentions/list/) | 提及了某个账号的帖子，从新到旧，每页 20 条：正文、作者、发布时间、浏览、点赞和转推。 | 每条 $0.0003（最少 $0.0003） | `GET /v1/x/users/mentions/list` |
| [X 列表帖子](https://okdata.online/zh/apis/x/lists/posts/list/) | 某个列表的时间线，从新到旧，每页约 100 条：正文、作者、发布时间、浏览、点赞和转推。 | $0.002 / 次 | `GET /v1/x/lists/posts/list` |
| [X 列表成员](https://okdata.online/zh/apis/x/lists/members/list/) | 某个列表收录的账号，每页 20 个：用户名、名称、简介、粉丝数和认证。 | 每条 $0.0004（最少 $0.0004） | `GET /v1/x/lists/members/list` |
| [X 列表关注者](https://okdata.online/zh/apis/x/lists/followers/list/) | 关注了某个列表的账号，最多 20 个：用户名、名称、简介、粉丝数和认证。只有这一页，不能往后翻。 | 每条 $0.0004（最少 $0.0004） | `GET /v1/x/lists/followers/list` |
| [X 社群资料](https://okdata.online/zh/apis/x/communities/get/) | 按 ID 取一个社群：名称、简介、成员数、创建时间，ext 里还有管理员人数、加入方式和主题。 | $0.0004 / 次 | `GET /v1/x/communities/get` |
| [X 社群帖子](https://okdata.online/zh/apis/x/communities/posts/list/) | 一个社群里的帖子，从新到旧，每页 20 条：正文、作者、发布时间、浏览、点赞和转推。 | 每条 $0.0003（最少 $0.0003） | `GET /v1/x/communities/posts/list` |
| [X 社群成员](https://okdata.online/zh/apis/x/communities/members/list/) | 加入了某个社群的账号，每页 20 个：用户名、名称、简介、粉丝数和认证。 | 每条 $0.0004（最少 $0.0004） | `GET /v1/x/communities/members/list` |

## 快速开始

1. 在 [okdata 控制台](https://okdata.online/zh/signup/?src=gh-x-twitter-api) 用邮箱注册，拿到 `okd_` 开头的 Key。
2. 调一次接口：

```bash
export OKDATA_API_KEY=okd_...
curl -G "https://api.okdata.online/v1/x/posts/search" \
  -H "Authorization: Bearer $OKDATA_API_KEY" \
  --data-urlencode 'query="claude code" lang:zh'
```

Python 版在 [examples/quickstart.py](examples/quickstart.py)（只用标准库，会顺带演示翻页）：`python3 examples/quickstart.py`。

返回统一的结构：列表在 `data.items`，下一页用 `page.next_cursor` 传回 `cursor`，这次扣了多少钱在 `meta.billing.amount`，平台不提供的字段为 null 并在 `meta.unavailable` 里写明原因。

## 让 AI 直接用（MCP）

Claude Code：

```bash
claude mcp add --transport http --scope user okdata https://api.okdata.online/mcp --header "Authorization: Bearer $OKDATA_API_KEY"
```

Cursor、Cherry Studio、WorkBuddy 等支持远程 MCP 的客户端：

```json
{
  "mcpServers": {
    "okdata": {
      "url": "https://api.okdata.online/mcp",
      "headers": {
        "Authorization": "Bearer okd_..."
      }
    }
  }
}
```

接好以后直接用中文说需求，比如「X 帖子搜索："claude code" lang:zh」。AI 会先用免费的 `find`、`describe` 找接口和看价格，再用 `call` 取数据。

## 常见问题

**要登录平台账号吗？** 不用。数据是公开内容，okdata 在服务端获取，你的账号完全不参与。

**怎么收费？** 每个接口单独定价，表里写的就是一次调用的价格；按条计费的接口按实际返回条数算。调用失败（包括超时）不扣费。新账号送 $0.1 试用额度，之后按需充值，没有订阅。价格页：https://okdata.online/zh/pricing/

**和官方开放平台有什么区别？** 官方开放平台只能读授权给你的账号自己的数据，而且要企业资质和审核；这里是平台上任何人都能看到的公开数据，比如搜索结果、别人的笔记或视频、评论、热榜。

**能翻页吗？** 列表接口每页一次调用，把 `page.next_cursor` 原样传回 `cursor` 就是下一页，24 小时内有效。

**出错了怎么办？** 每个错误都有固定的 `code`、中文说明 `message_zh`，以及会不会扣费（`charged`）和要不要重试（`retry`）。全部错误码：https://okdata.online/zh/docs/errors/

## English

Examples for the okdata X (Twitter) API: 20 live endpoints behind one API key, pay per call from $0.0001, failed calls free, no platform login or cookies. Sign up at https://okdata.online/signup/?src=gh-x-twitter-api, docs at https://okdata.online/apis/, MCP at https://okdata.online/mcp/.

## License

MIT. The data comes from the okdata API; its terms apply to API use.
