# GoT Quotes: List Characters



```
GET https://connect.mindcloud.co/v1/universal/goTQuotes/latest/actions/list-characters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoT Quotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTQuotes/latest/actions/list-characters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTQuotes/latest/actions/list-characters?${params}`, {
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
          "house": {
            "name": "Ava Chen",
            "slug": "string"
          },
          "name": "Ava Chen",
          "quotes": [
            "string"
          ],
          "slug": "string"
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
| `[].house` | object |  |
| `[].house.name` | string |  |
| `[].house.slug` | string |  |
| `[].name` | string |  |
| `[].quotes` | array<string> |  |
| `[].slug` | string |  |

## Native endpoint

Through the native GoT Quotes API, this operation is `GET /v1/characters` (base URL `https://api.gameofthronesquotes.xyz`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-characters.md) for the provider-specific parameters and requirements.

