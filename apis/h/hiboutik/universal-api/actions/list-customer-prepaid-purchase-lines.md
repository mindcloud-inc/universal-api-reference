# Hiboutik: List Customer Prepaid Purchase Lines

Retrieves prepaid purchase lines for a customer in Hiboutik.

```
GET https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-customer-prepaid-purchase-lines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hiboutik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-customer-prepaid-purchase-lines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-customer-prepaid-purchase-lines?${params}`, {
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
| `customersId` | string | no | The Hiboutik customer id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "customersId": 1,
      "paymentId": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `customersId` | number |  |
| `paymentId` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Hiboutik API, this operation is `GET /prepaid_purchases/:customers_id` (base URL `https://mindcloudhiboutik20260402.hiboutik.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-prepaid-purchase-lines.md) for the provider-specific parameters and requirements.

