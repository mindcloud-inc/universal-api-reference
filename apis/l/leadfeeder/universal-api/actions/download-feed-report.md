# Leadfeeder: Download Feed Report

Retrieves a feed export report from Leadfeeder.

```
GET https://connect.mindcloud.co/v1/universal/leadfeeder/latest/actions/download-feed-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadfeeder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadfeeder/latest/actions/download-feed-report?connectionId=$CONNECTION_ID&uniqueFilename=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uniqueFilename": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadfeeder/latest/actions/download-feed-report?${params}`, {
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
| `uniqueFilename` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "keywords": [
          "string"
        ],
        "quality": 1,
        "stats": {
          "bounces": 1,
          "last_visit": "string",
          "pageviews": 1,
          "visits": 1
        }
      },
      "id": "string",
      "relationships": {
        "lead": {
          "data": {
            "id": "string",
            "type": "string"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.keywords` | array<string> |  |
| `attributes.quality` | number |  |
| `attributes.stats` | object |  |
| `attributes.stats.bounces` | number |  |
| `attributes.stats.last_visit` | string |  |
| `attributes.stats.pageviews` | number |  |
| `attributes.stats.visits` | number |  |
| `id` | string |  |
| `relationships.lead.data.id` | string |  |
| `relationships.lead.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Leadfeeder API, this operation is `GET /download/:uniqueFilename` (base URL `https://api.leadfeeder.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-feed-report.md) for the provider-specific parameters and requirements.

