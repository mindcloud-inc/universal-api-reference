# Final Space: List Episodes



```
GET https://connect.mindcloud.co/v1/universal/finalSpace/latest/actions/list-episodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Final Space `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finalSpace/latest/actions/list-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finalSpace/latest/actions/list-episodes?${params}`, {
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
      "": [
        {
          "air_date": "string",
          "characters": [
            "string"
          ],
          "director": "string",
          "id": 1,
          "img_url": "https://example.com",
          "name": "Ava Chen",
          "writer": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[]` | array<object> |  |
| `[].air_date` | string |  |
| `[].characters` | array<string> |  |
| `[].director` | string |  |
| `[].id` | number |  |
| `[].img_url` | string |  |
| `[].name` | string |  |
| `[].writer` | string |  |

## Native endpoint

Through the native Final Space API, this operation is `GET /episode` (base URL `https://finalspaceapi.com/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-episodes.md) for the provider-specific parameters and requirements.

