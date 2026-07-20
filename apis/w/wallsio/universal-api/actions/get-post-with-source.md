# Walls.io: Get Post With Source

Retrieves a post with source details from Walls.io.

```
GET https://connect.mindcloud.co/v1/universal/wallsio/latest/actions/get-post-with-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walls.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wallsio/latest/actions/get-post-with-source?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wallsio/latest/actions/get-post-with-source?${params}`, {
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
| `postId` | string | no | Walls.io post ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "current_time": 1,
      "data": {},
      "info": [
        "string"
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_time` | number |  |
| `data` | object |  |
| `info` | array<string> |  |
| `status` | string |  |

## Native endpoint

Through the native Walls.io API, this operation is `GET /posts/:postId` (base URL `https://api.walls.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-post-with-source.md) for the provider-specific parameters and requirements.

