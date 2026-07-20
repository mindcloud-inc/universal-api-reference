# LeadDyno: Retrieve Purchase Commissions

Retrieves commissions for a specific purchase in LeadDyno.

```
GET https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/retrieve-purchase-commissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadDyno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/retrieve-purchase-commissions?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/retrieve-purchase-commissions?${params}`, {
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
| `id` | number | yes | The purchase ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "cancelled": true,
      "currency": "string",
      "id": 1,
      "paid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `cancelled` | boolean |  |
| `currency` | string |  |
| `id` | number |  |
| `paid` | boolean |  |

## Native endpoint

Through the native LeadDyno API, this operation is `GET /purchases/:id/commissions` (base URL `https://api.leaddyno.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-purchase-commissions.md) for the provider-specific parameters and requirements.

