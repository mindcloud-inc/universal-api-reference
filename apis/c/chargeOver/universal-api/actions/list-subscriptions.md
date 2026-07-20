# ChargeOver: List Subscriptions

Retrieves billing subscription records from ChargeOver.

```
GET https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeOver `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/list-subscriptions?${params}`, {
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
| `expand` | string | no | Optional comma-separated related objects to expand in the subscription response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount_collected": 1,
      "amount_due": 1,
      "amount_invoiced": 1,
      "arr": 1,
      "cancel_datetime": "string",
      "customer_id": 1,
      "mrr": 1,
      "next_invoice_datetime": "string",
      "package_id": 1,
      "package_status_name": "Ava Chen",
      "paycycle_name": "Ava Chen",
      "paymethod_name": "Ava Chen",
      "url_self": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount_collected` | number |  |
| `amount_due` | number |  |
| `amount_invoiced` | number |  |
| `arr` | number |  |
| `cancel_datetime` | string |  |
| `customer_id` | number |  |
| `mrr` | number |  |
| `next_invoice_datetime` | string |  |
| `package_id` | number |  |
| `package_status_name` | string |  |
| `paycycle_name` | string |  |
| `paymethod_name` | string |  |
| `url_self` | string |  |

## Native endpoint

Through the native ChargeOver API, this operation is `GET /package` (base URL `https://{{credentials.siteName}}.chargeover.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

