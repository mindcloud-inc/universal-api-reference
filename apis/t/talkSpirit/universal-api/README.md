# <img src="https://images.mindcloud.co/apps/icons/talk-spirit_1774556009509.png" alt="talkSpirit logo" width="28" height="28"> talkSpirit: Universal API

Send talkSpirit posts and threaded updates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/talkSpirit/latest
- **Category:** Communication / Team Messaging
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.talkspirit.com
- **Vendor API docs:** https://talkspirit.github.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Send Post](actions/send-post.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/talkSpirit/latest/actions/send-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string"
}'
```

## Actions (1)

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Post](actions/send-post.md) | POST | Creates a new post in talkSpirit via incoming webhook. |

