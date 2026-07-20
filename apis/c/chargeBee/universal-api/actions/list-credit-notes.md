# ChargeBee: List Credit Notes

Retrieves credit notes from ChargeBee.

```
GET https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/list-credit-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeBee `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/list-credit-notes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/list-credit-notes?${params}`, {
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
      "currency_code": "string",
      "customer_id": "string",
      "date": 1,
      "id": "string",
      "object": "string",
      "reason_code": "string",
      "status": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency_code` | string |  |
| `customer_id` | string |  |
| `date` | number |  |
| `id` | string |  |
| `object` | string |  |
| `reason_code` | string |  |
| `status` | string |  |
| `total` | number |  |

## Native endpoint

Through the native ChargeBee API, this operation is `GET credit_notes` (base URL `https://{{credentials.baseUrl}}.chargebee.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-credit-notes.md) for the provider-specific parameters and requirements.

