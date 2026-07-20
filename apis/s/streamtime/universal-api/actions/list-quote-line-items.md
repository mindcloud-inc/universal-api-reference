# Streamtime: List Quote Line Items



```
GET https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/list-quote-line-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamtime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/list-quote-line-items?connectionId=$CONNECTION_ID&quoteId=1433522" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "quoteId": "1433522"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/list-quote-line-items?${params}`, {
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
| `quoteId` | number | yes | Quote ID. Example: `1433522`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountCode": "string",
      "active": true,
      "description": "string",
      "externalTaxRateId": "string",
      "id": 1,
      "name": "Ava Chen",
      "orderId": 1,
      "quantity": "string",
      "quoteId": 1,
      "taxName": "Ava Chen",
      "taxRate": 1,
      "totalAmountExTax": 1,
      "unitRate": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountCode` | string | Accounting account code |
| `active` | boolean | Whether the line item is active |
| `description` | string | Line item description |
| `externalTaxRateId` | string | External tax rate ID |
| `id` | number | Quote line item ID |
| `name` | string | Line item name |
| `orderId` | number | Display order |
| `quantity` | string | Quoted quantity |
| `quoteId` | number | Parent quote ID |
| `taxName` | string | Tax name |
| `taxRate` | number | Tax rate |
| `totalAmountExTax` | number | Total amount excluding tax |
| `unitRate` | number | Unit rate |

## Native endpoint

Through the native Streamtime API, this operation is `GET /quotes/:quote_id/quote_line_items` (base URL `https://api.streamtime.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-quote-line-items.md) for the provider-specific parameters and requirements.

