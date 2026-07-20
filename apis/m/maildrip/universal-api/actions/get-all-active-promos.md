# Maildrip: Get all active promos



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-all-active-promos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-all-active-promos?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-all-active-promos?${params}`, {
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
      "count": 1,
      "promos": [
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
| `count` | number |  |
| `promos` | array<object> |  |

## Native endpoint

Through the native Maildrip API, this operation is `GET /api/v1/promo/active` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-active-promos.md) for the provider-specific parameters and requirements.

