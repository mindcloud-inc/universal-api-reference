# LeadDyno: Retrieve Affiliate Commissions

Retrieves commissions for a specific affiliate in LeadDyno.

```
GET https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/retrieve-affiliate-commissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadDyno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/retrieve-affiliate-commissions?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/retrieve-affiliate-commissions?${params}`, {
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
      "affiliate": {},
      "amount": "string",
      "cancelled": true,
      "created_at": "string",
      "currency": "string",
      "date": "string",
      "due_at": "string",
      "id": 1,
      "note": "string",
      "paid": true,
      "purchase": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliate` | object |  |
| `amount` | string |  |
| `cancelled` | boolean |  |
| `created_at` | string |  |
| `currency` | string |  |
| `date` | string |  |
| `due_at` | string |  |
| `id` | number |  |
| `note` | string |  |
| `paid` | boolean |  |
| `purchase` | object |  |

## Native endpoint

Through the native LeadDyno API, this operation is `GET /affiliates/:id/commissions` (base URL `https://api.leaddyno.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-affiliate-commissions.md) for the provider-specific parameters and requirements.

