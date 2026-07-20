# Kiwify: Get Sales Stats

Retrieves sales statistics from Kiwify.

```
GET https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/get-sales-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/get-sales-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/get-sales-stats?${params}`, {
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
| `productId` | string | no |  |
| `startDate` | string | no |  |
| `endDate` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "boleto_rate": 1,
      "chargeback_rate": 1,
      "credit_card_approval_rate": 1,
      "refund_rate": 1,
      "total_boleto_generated": 1,
      "total_boleto_paid": 1,
      "total_net_amount": 1,
      "total_sales": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `boleto_rate` | number |  |
| `chargeback_rate` | number |  |
| `credit_card_approval_rate` | number |  |
| `refund_rate` | number |  |
| `total_boleto_generated` | number |  |
| `total_boleto_paid` | number |  |
| `total_net_amount` | number |  |
| `total_sales` | number |  |

## Native endpoint

Through the native Kiwify API, this operation is `GET /v1/stats` (base URL `https://public-api.kiwify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sales-stats.md) for the provider-specific parameters and requirements.

