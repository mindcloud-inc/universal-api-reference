# LeadDyno: Retrieve Affiliate Purchases

Retrieves purchases for a specific affiliate in LeadDyno.

```
GET https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/retrieve-affiliate-purchases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadDyno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/retrieve-affiliate-purchases?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/retrieve-affiliate-purchases?${params}`, {
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
| `id` | number | yes | The affiliate ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancelled": true,
      "currency": "string",
      "id": 1,
      "purchase_amount": "string",
      "purchase_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancelled` | boolean |  |
| `currency` | string |  |
| `id` | number |  |
| `purchase_amount` | string |  |
| `purchase_code` | string |  |

## Native endpoint

Through the native LeadDyno API, this operation is `GET /affiliates/:id/purchases` (base URL `https://api.leaddyno.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-affiliate-purchases.md) for the provider-specific parameters and requirements.

