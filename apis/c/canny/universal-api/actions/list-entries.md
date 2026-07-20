# Canny: List Entries

Retrieves all available entries from Canny.

```
GET https://connect.mindcloud.co/v1/universal/canny/latest/actions/list-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canny `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/canny/latest/actions/list-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/canny/latest/actions/list-entries?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "labels": [
        {}
      ],
      "lastSaved": "2026-05-07T12:00:00.000Z",
      "markdownDetails": "string",
      "plaintextDetails": "string",
      "posts": [
        {}
      ],
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "reactions": {},
      "scheduledFor": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "title": "string",
      "types": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `id` | string |  |
| `labels` | array<object> |  |
| `lastSaved` | date |  |
| `markdownDetails` | string |  |
| `plaintextDetails` | string |  |
| `posts` | array<object> |  |
| `publishedAt` | date |  |
| `reactions` | object |  |
| `scheduledFor` | date |  |
| `status` | string |  |
| `title` | string |  |
| `types` | array<string> |  |
| `url` | string |  |

## Native endpoint

Through the native Canny API, this operation is `POST /v1/entries/list` (base URL `https://canny.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-entries.md) for the provider-specific parameters and requirements.

