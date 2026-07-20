# LeadDyno: Retrieve Commission Totals

Retrieves commission totals from your LeadDyno account.

```
GET https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/retrieve-commission-totals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadDyno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/retrieve-commission-totals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadDyno/latest/actions/retrieve-commission-totals?${params}`, {
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
| `currency` | string | no | The commission currency code. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `affiliate_id` | number | no | The affiliate ID whose commissions are to be retrieved. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "total_cancelled_count": 1,
      "total_cost": "string",
      "total_count": 1,
      "total_due_cost": "string",
      "total_due_count": 1,
      "total_paid_cost": "string",
      "total_paid_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `total_cancelled_count` | number |  |
| `total_cost` | string |  |
| `total_count` | number |  |
| `total_due_cost` | string |  |
| `total_due_count` | number |  |
| `total_paid_cost` | string |  |
| `total_paid_count` | number |  |

## Native endpoint

Through the native LeadDyno API, this operation is `GET /commissions/totals` (base URL `https://api.leaddyno.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-commission-totals.md) for the provider-specific parameters and requirements.

