# X (Twitter) API: post search, replies, accounts, followers, trends and communities

**X API · Twitter API · tweet search with X search operators · tweet replies and quotes · Twitter followers · X trends · X lists and communities.**

Examples for the [okdata](https://okdata.online/?src=gh-x-twitter-api) X (Twitter) API: 20 live endpoints behind one API key, pay per call from $0.0001. No X (Twitter) login, no cookies and no browser, so there is no account to get blocked.

[Sign up free ($0.10 of trial credit)](https://okdata.online/signup/?src=gh-x-twitter-api) · [All X (Twitter) endpoints](https://okdata.online/apis/x/?src=gh-x-twitter-api) · [Use it from Claude, Cursor or any MCP client](https://okdata.online/mcp/?src=gh-x-twitter-api)

## Endpoints

| Endpoint | What it returns | Price | Path |
|---|---|---|---|
| [X post detail](https://okdata.online/apis/x/posts/get/?src=gh-x-twitter-api) | One post by ID or link: text, media, views, likes, reposts and replies. | $0.0003 a call | `GET /v1/x/posts/get` |
| [X post search](https://okdata.online/apis/x/posts/search/?src=gh-x-twitter-api) | Posts matching a query (X search operators work), latest or top. | $0.002 a call | `GET /v1/x/posts/search` |
| [X account profile](https://okdata.online/apis/x/users/get/?src=gh-x-twitter-api) | An account by handle or numeric ID, or up to 100 accounts by ID in one call: followers, following, post count, bio and verification. IDs that find no account are listed under data.missing and not charged; a batch that finds none costs one account. | $0.0004 per item (at least $0.0004) | `GET /v1/x/users/get` |
| [X account posts](https://okdata.online/apis/x/users/posts/list/?src=gh-x-twitter-api) | An account's posts, newest first. | $0.002 a call | `GET /v1/x/users/posts/list` |
| [X trending topics](https://okdata.online/apis/x/trends/list/?src=gh-x-twitter-api) | Trending topics worldwide or for one country. | $0.009 a call | `GET /v1/x/trends/list` |
| [X post replies](https://okdata.online/apis/x/posts/replies/list/?src=gh-x-twitter-api) | The replies under a post, in the order X ranks them, about 35 a page. A reply is a post itself, so each comes back as a post: text, author, time posted, views, likes and its own reply count. | $0.002 a call | `GET /v1/x/posts/replies/list` |
| [X post quotes](https://okdata.online/apis/x/posts/quotes/list/?src=gh-x-twitter-api) | Posts that quote a post, newest or most popular first, 20 a page: what people added, who they are and how far it went. | $0.0003 per item (at least $0.0003) | `GET /v1/x/posts/quotes/list` |
| [X post retweeters](https://okdata.online/apis/x/posts/retweeters/list/?src=gh-x-twitter-api) | The accounts that retweeted a post, about 100 a page: handle, name, bio and follower count. | $0.002 a call | `GET /v1/x/posts/retweeters/list` |
| [X article](https://okdata.online/apis/x/posts/article/get/?src=gh-x-twitter-api) | The long-form article attached to a post, by the post ID: title, the whole text, author, time published, views, likes and replies. | $0.002 a call | `GET /v1/x/posts/article/get` |
| [X thread](https://okdata.online/apis/x/threads/posts/list/?src=gh-x-twitter-api) | The posts of a thread, from the ID of any post in it: the post it started from, the author's follow-ups and the replies in between. X sets the page size, up to about 50. | $0.0003 per item (at least $0.0003) | `GET /v1/x/threads/posts/list` |
| [X account search](https://okdata.online/apis/x/users/search/?src=gh-x-twitter-api) | Accounts matching keywords, 20 a page: handle, name, bio, followers, following, post count and verification. | $0.0004 per item (at least $0.0004) | `GET /v1/x/users/search` |
| [X account followers](https://okdata.online/apis/x/users/followers/list/?src=gh-x-twitter-api) | The accounts following an account, newest followers first, 200 a page: handle, name, bio, followers and post count. | $0.0001 per item (at least $0.0004) | `GET /v1/x/users/followers/list` |
| [X account following](https://okdata.online/apis/x/users/following/list/?src=gh-x-twitter-api) | The accounts an account follows, most recently followed first, 200 a page: handle, name, bio, followers and post count. | $0.0001 per item (at least $0.0004) | `GET /v1/x/users/following/list` |
| [X account mentions](https://okdata.online/apis/x/users/mentions/list/?src=gh-x-twitter-api) | Posts that mention an account, newest first, 20 a page: text, author, time posted, views, likes and reposts. | $0.0003 per item (at least $0.0003) | `GET /v1/x/users/mentions/list` |
| [X list posts](https://okdata.online/apis/x/lists/posts/list/?src=gh-x-twitter-api) | The timeline of a list, newest first, about 100 posts a page: text, author, time posted, views, likes and reposts. | $0.002 a call | `GET /v1/x/lists/posts/list` |
| [X list members](https://okdata.online/apis/x/lists/members/list/?src=gh-x-twitter-api) | The accounts a list is made of, 20 a page: handle, name, bio, followers and verification. | $0.0004 per item (at least $0.0004) | `GET /v1/x/lists/members/list` |
| [X list followers](https://okdata.online/apis/x/lists/followers/list/?src=gh-x-twitter-api) | Up to 20 accounts that follow a list: handle, name, bio, followers and verification. One page only; there is no next page. | $0.0004 per item (at least $0.0004) | `GET /v1/x/lists/followers/list` |
| [X community profile](https://okdata.online/apis/x/communities/get/?src=gh-x-twitter-api) | A community by ID: name, description, member count, when it was created, and under ext its moderators, how people join and its topic. | $0.0004 a call | `GET /v1/x/communities/get` |
| [X community posts](https://okdata.online/apis/x/communities/posts/list/?src=gh-x-twitter-api) | Posts in a community, newest first, 20 a page: text, author, time posted, views, likes and reposts. | $0.0003 per item (at least $0.0003) | `GET /v1/x/communities/posts/list` |
| [X community members](https://okdata.online/apis/x/communities/members/list/?src=gh-x-twitter-api) | The accounts that have joined a community, 20 a page: handle, name, bio, followers and verification. | $0.0004 per item (at least $0.0004) | `GET /v1/x/communities/members/list` |

## Quick start

1. Sign up at the [okdata console](https://okdata.online/signup/?src=gh-x-twitter-api) with your email and copy the key that starts with `okd_`.
2. Make a call:

```bash
export OKDATA_API_KEY=okd_...
curl -G "https://api.okdata.online/v1/x/posts/search" \
  -H "Authorization: Bearer $OKDATA_API_KEY" \
  --data-urlencode 'query="claude code" lang:zh'
```

The Python version is [examples/quickstart.py](examples/quickstart.py) (standard library only, and it fetches a second page too): `python3 examples/quickstart.py`.

Every endpoint answers in the same shape: the list is in `data.items`, `page.next_cursor` goes back as `cursor` for the next page, what the call cost is in `meta.billing.amount`, and a field the platform does not provide is null with the reason in `meta.unavailable`.

## Use it from AI (MCP)

Claude Code:

```bash
claude mcp add --transport http --scope user okdata https://api.okdata.online/mcp --header "Authorization: Bearer $OKDATA_API_KEY"
```

Cursor, Windsurf, VS Code and other clients with remote MCP:

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

Then ask in plain words, for example "X post search: "claude code" lang:zh". The agent uses the free `find` and `describe` tools to pick the endpoint and see its price, then `call` to fetch the data.

## FAQ

**Do I need a X (Twitter) account?** No. The data is public content, fetched on the server; your own account is never involved.

**How is it billed?** Each endpoint has its own price, listed above for one call; endpoints billed per item count what comes back. New accounts get $0.10 to try; after that, top-ups start at $10 and never expire, with no subscription. Pricing: https://okdata.online/pricing/?src=gh-x-twitter-api · Billing details: https://okdata.online/docs/billing/?src=gh-x-twitter-api

**Do I need an X developer account?** No. One okdata key and no plan to pick: you pay for the calls you make from a prepaid balance.

**Can I page through results?** Each page of a list is one call: pass `page.next_cursor` back as `cursor` for the next one. A cursor stays valid for 24 hours.

**What happens when a call fails?** Every error has a fixed `code`, a `message`, and says whether you were charged (`charged`) and whether to retry (`retry`). All error codes: https://okdata.online/docs/errors/?src=gh-x-twitter-api

## 中文说明

**推特数据 API · X 帖子搜索 · 推文详情和回复 · 推特账号和粉丝 · X 趋势 · X 列表和社群。**

okdata 的X（推特）接口示例：20 个接口在线可用，一个 API Key 调用，按次计费（$0.0001 起），不用登录平台账号、不用 Cookie。中文文档：https://okdata.online/zh/apis/x/?src=gh-x-twitter-api · 注册：https://okdata.online/zh/signup/?src=gh-x-twitter-api · 接入 AI（MCP）：https://okdata.online/zh/mcp/?src=gh-x-twitter-api

## License

MIT. The data comes from the okdata API; its terms apply to API use.
