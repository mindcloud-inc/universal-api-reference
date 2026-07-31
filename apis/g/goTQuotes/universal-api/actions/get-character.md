# GoT Quotes: Get Character



```
GET https://connect.mindcloud.co/v1/universal/goTQuotes/latest/actions/get-character
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoT Quotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTQuotes/latest/actions/get-character?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTQuotes/latest/actions/get-character?${params}`, {
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
| `slug` | string | yes |  |

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

Through the native GoT Quotes API, this operation is `GET /v1/character/:slug` (base URL `https://api.gameofthronesquotes.xyz`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-character.md) for the provider-specific parameters and requirements.

