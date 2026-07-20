# Ayrshare: List Post History

Retrieves post history from Ayrshare.

```
GET https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/list-post-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/list-post-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/list-post-history?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lastDays` | number | no | Return posts from the last number of days. Use 0 to return all history constrained by the limit. |
| `platforms[]` | array<string> | no | Filter by one or more Ayrshare platform values. |
| `status` | string | no | Filter by post status such as success, error, pending, paused, deleted, or awaiting approval. One of: `awaiting approval`, `deleted`, `error`, `paused`, `pending`, `processing`, `success`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "history": [
        {}
      ],
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "nextUpdate": "2026-05-07T12:00:00.000Z",
      "refId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of returned history records. |
| `history` | array<object> | Post history records returned by Ayrshare. |
| `lastUpdated` | date | History cache update timestamp. |
| `nextUpdate` | date | Next history cache update timestamp. |
| `refId` | string | Ayrshare profile reference ID. |

## Native endpoint

Through the native Ayrshare API, this operation is `GET /history` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-post-history.md) for the provider-specific parameters and requirements.

