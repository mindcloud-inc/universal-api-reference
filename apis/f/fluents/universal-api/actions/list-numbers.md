# Fluents: List Numbers

Retrieves phone numbers from your Fluents account.

```
GET https://connect.mindcloud.co/v1/universal/fluents/latest/actions/list-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fluents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fluents/latest/actions/list-numbers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fluents/latest/actions/list-numbers?${params}`, {
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
      "has_more": true,
      "items": [
        {}
      ],
      "page": 1,
      "size": 1,
      "total": 1,
      "total_is_estimated": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `has_more` | boolean |  |
| `items` | array<object> |  |
| `page` | number |  |
| `size` | number |  |
| `total` | number |  |
| `total_is_estimated` | boolean |  |

## Native endpoint

Through the native Fluents API, this operation is `GET /numbers/list` (base URL `https://api.fluents.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-numbers.md) for the provider-specific parameters and requirements.

