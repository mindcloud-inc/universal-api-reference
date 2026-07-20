# Evervault: List Merchants

Retrieves all payment merchants from Evervault.

```
GET https://connect.mindcloud.co/v1/universal/evervault/latest/actions/list-merchants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evervault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evervault/latest/actions/list-merchants?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evervault/latest/actions/list-merchants?${params}`, {
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
      "data": [
        {}
      ],
      "nextPage": "string",
      "pageSize": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | List of merchant objects. |
| `nextPage` | string |  |
| `pageSize` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Evervault API, this operation is `GET /payments/merchants` (base URL `https://api.evervault.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-merchants.md) for the provider-specific parameters and requirements.

