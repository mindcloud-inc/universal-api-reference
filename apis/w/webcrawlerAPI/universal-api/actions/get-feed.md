# Webcrawler API: Get Feed

Retrieves feed details and recent runs from Webcrawler API.

```
GET https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/get-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webcrawler API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/get-feed?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/get-feed?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Feed identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "intervalMinutes": 1,
      "itemsLimit": 1,
      "lastRunAt": "string",
      "name": "Ava Chen",
      "nextRunAt": "string",
      "recentRuns": [
        {}
      ],
      "scrapeType": "string",
      "status": "string",
      "url": "https://example.com",
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Feed creation timestamp. |
| `id` | string | Feed identifier. |
| `intervalMinutes` | number | Feed polling interval in minutes. |
| `itemsLimit` | number | Configured item limit for the feed. |
| `lastRunAt` | string | Timestamp of the last completed run when available. |
| `name` | string | Feed display name when configured. |
| `nextRunAt` | string | Timestamp of the next scheduled run when available. |
| `recentRuns` | array<object> | Recent feed run summaries returned by the provider. |
| `scrapeType` | string | Configured feed output format. |
| `status` | string | Current feed status. |
| `url` | string | Configured feed URL. |
| `webhookUrl` | string | Webhook URL configured for the feed when available. |

## Native endpoint

Through the native Webcrawler API API, this operation is `GET /v2/feed/:id` (base URL `https://api.webcrawlerapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feed.md) for the provider-specific parameters and requirements.

