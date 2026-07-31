# GoT Quotes: List Houses



```
GET https://connect.mindcloud.co/v1/universal/goTQuotes/latest/actions/list-houses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoT Quotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTQuotes/latest/actions/list-houses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTQuotes/latest/actions/list-houses?${params}`, {
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
          "members": [
            {
              "name": "Ava Chen",
              "slug": "string"
            }
          ],
          "name": "Ava Chen",
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
| `[].members` | array<object> |  |
| `[].members[].name` | string |  |
| `[].members[].slug` | string |  |
| `[].name` | string |  |
| `[].slug` | string |  |

## Native endpoint

Through the native GoT Quotes API, this operation is `GET /v1/houses` (base URL `https://api.gameofthronesquotes.xyz`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-houses.md) for the provider-specific parameters and requirements.

