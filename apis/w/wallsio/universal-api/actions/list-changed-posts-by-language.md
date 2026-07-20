# Walls.io: List Changed Posts By Language

Finds updated posts in Walls.io by language.

```
GET https://connect.mindcloud.co/v1/universal/wallsio/latest/actions/list-changed-posts-by-language
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walls.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wallsio/latest/actions/list-changed-posts-by-language?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wallsio/latest/actions/list-changed-posts-by-language?${params}`, {
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
| `languages` | string | no | Comma-separated ISO 639-1 language codes to include. |
| `since` | string | no | UNIX timestamp; returns posts changed after this time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "current_time": 1,
      "data": [
        {}
      ],
      "info": [
        "string"
      ],
      "query": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `current_time` | number |  |
| `data` | array<object> |  |
| `info` | array<string> |  |
| `query` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Walls.io API, this operation is `GET /posts/changed` (base URL `https://api.walls.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-changed-posts-by-language.md) for the provider-specific parameters and requirements.

