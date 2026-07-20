# <img src="https://images.mindcloud.co/apps/icons/chip-bot_1774893832584.png" alt="ChipBot logo" width="28" height="28"> ChipBot: Universal API

ChipBot combines video experiences, live chat, help-desk content, and reporting for customer-facing websites. This connector focuses on the currently documented HTTP API surface for domain-level video, messaging, help-desk, and reporting workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chipBot/latest
- **Category:** Support / Customer Success
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://getchipbot.com/
- **Vendor API docs:** https://getchipbot.com/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Connect Domain](actions/connect-domain.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/connect-domain?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Article

| Action | Method | Description |
| --- | --- | --- |
| [List Articles](actions/list-articles.md) | GET |  |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Connect Domain](actions/connect-domain.md) | GET |  |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Reply to Message](actions/reply-to-message.md) | POST |  |

### Thread

| Action | Method | Description |
| --- | --- | --- |
| [Get Thread](actions/get-thread.md) | GET |  |

### Unique Hits

| Action | Method | Description |
| --- | --- | --- |
| [Get Detailed Unique Hits Report](actions/get-detailed-unique-hits-report.md) | GET |  |
| [Get Unique Hits Report](actions/get-unique-hits-report.md) | GET |  |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Delete Video](actions/delete-video.md) | DELETE |  |
| [Get Video](actions/get-video.md) | GET |  |
| [List Videos](actions/list-videos.md) | GET |  |

### Video Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Detailed Video Analytics](actions/get-detailed-video-analytics.md) | GET |  |
| [Get Video Analytics Summary](actions/get-video-analytics-summary.md) | GET |  |
| [Get Video Analytics Views by URL](actions/get-video-analytics-views-by-url.md) | GET |  |

### Video Upload

| Action | Method | Description |
| --- | --- | --- |
| [Request Video Service Token](actions/request-video-service-token.md) | GET |  |
| [Request Video Upload Token](actions/request-video-upload-token.md) | POST |  |

