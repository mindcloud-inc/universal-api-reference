# ChargeOver: Get Subscription

Retrieves detailed subscription records from ChargeOver.

```
GET https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/get-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeOver `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/get-subscription?connectionId=$CONNECTION_ID&packageId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "packageId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/get-subscription?${params}`, {
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
| `packageId` | number | yes | The ChargeOver subscription ID. |

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

Through the native ChargeOver API, this operation is `GET /package/:package_id` (base URL `https://{{credentials.siteName}}.chargeover.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscription.md) for the provider-specific parameters and requirements.

