# Dify: Get App Info

Retrieves application info from Dify.

```
GET https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-app-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-app-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dify/latest/actions/get-app-info?${params}`, {
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
      "authorName": "Ava Chen",
      "description": "string",
      "mode": "string",
      "name": "Ava Chen",
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorName` | string |  |
| `description` | string |  |
| `mode` | string |  |
| `name` | string |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native Dify API, this operation is `GET /info` (base URL `https://api.dify.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app-info.md) for the provider-specific parameters and requirements.

