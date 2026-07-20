# Runn: List Rate Cards



```
GET https://connect.mindcloud.co/v1/universal/runn/latest/actions/list-rate-cards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runn/latest/actions/list-rate-cards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runn/latest/actions/list-rate-cards?${params}`, {
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
      "nextCursor": "string",
      "values": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextCursor` | string | Cursor for the next page of results, or null. |
| `values` | array<object> | Rate cards returned by the API. |

## Native endpoint

Through the native Runn API, this operation is `GET /rate-cards/` (base URL `https://api.runn.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-rate-cards.md) for the provider-specific parameters and requirements.

