# ChargeBee: List Promotional Credits

Retrieves promotional credits from ChargeBee.

```
GET https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/list-promotional-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeBee `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/list-promotional-credits?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/list-promotional-credits?${params}`, {
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
      "amount": 1,
      "created_at": 1,
      "currency_code": "string",
      "customer_id": "string",
      "description": "string",
      "id": "string",
      "object": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `created_at` | number |  |
| `currency_code` | string |  |
| `customer_id` | string |  |
| `description` | string |  |
| `id` | string |  |
| `object` | string |  |
| `type` | string |  |

## Native endpoint

Through the native ChargeBee API, this operation is `GET promotional_credits` (base URL `https://{{credentials.baseUrl}}.chargebee.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-promotional-credits.md) for the provider-specific parameters and requirements.

