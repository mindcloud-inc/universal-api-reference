# GoT Quotes: Get Random Quote



```
GET https://connect.mindcloud.co/v1/universal/goTQuotes/latest/actions/get-random-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoT Quotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTQuotes/latest/actions/get-random-quote?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTQuotes/latest/actions/get-random-quote?${params}`, {
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
      "character": {
        "house": {
          "name": "Ava Chen",
          "slug": "string"
        },
        "name": "Ava Chen",
        "slug": "string"
      },
      "sentence": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `character` | object |  |
| `character.house` | object |  |
| `character.house.name` | string |  |
| `character.house.slug` | string |  |
| `character.name` | string |  |
| `character.slug` | string |  |
| `sentence` | string |  |

## Native endpoint

Through the native GoT Quotes API, this operation is `GET /v1/random` (base URL `https://api.gameofthronesquotes.xyz`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-random-quote.md) for the provider-specific parameters and requirements.

