# LeadDyno: Retrieve Purchase By Code

Retrieves a purchase from LeadDyno by purchase code.

```
GET https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/retrieve-purchase-by-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadDyno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/retrieve-purchase-by-code?connectionId=$CONNECTION_ID&purchase_code=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "purchase_code": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/retrieve-purchase-by-code?${params}`, {
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
| `purchase_code` | string | yes | A unique identifier associated with the purchase to retrieve. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include_line_items` | boolean | no | Include detailed line items in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliate": {},
      "cancelled": true,
      "created_at": "string",
      "currency": "string",
      "id": 1,
      "lead": {},
      "plan": {},
      "purchase_amount": "string",
      "purchase_code": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliate` | object |  |
| `cancelled` | boolean |  |
| `created_at` | string |  |
| `currency` | string |  |
| `id` | number |  |
| `lead` | object |  |
| `plan` | object |  |
| `purchase_amount` | string |  |
| `purchase_code` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native LeadDyno API, this operation is `GET /purchases/by_purchase_code` (base URL `https://api.leaddyno.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-purchase-by-code.md) for the provider-specific parameters and requirements.

