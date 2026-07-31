# Final Space: List Quotes



```
GET https://connect.mindcloud.co/v1/universal/finalSpace/latest/actions/list-quotes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Final Space `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finalSpace/latest/actions/list-quotes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finalSpace/latest/actions/list-quotes?${params}`, {
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
          "by": "string",
          "character": "string",
          "id": 1,
          "image": "string",
          "quote": "string"
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
| `[].by` | string |  |
| `[].character` | string |  |
| `[].id` | number |  |
| `[].image` | string |  |
| `[].quote` | string |  |

## Native endpoint

Through the native Final Space API, this operation is `GET /quote` (base URL `https://finalspaceapi.com/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-quotes.md) for the provider-specific parameters and requirements.

