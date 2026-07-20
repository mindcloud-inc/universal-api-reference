# Lexware Office: Create Quotation

Creates a new quotation in Lexware Office.

```
POST https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/create-quotation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lexware Office `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/create-quotation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "voucherDate": "2026-05-07T12:00:00.000Z",
  "expirationDate": "2026-05-07T12:00:00.000Z",
  "address": {},
  "lineItems[]": [
    {}
  ],
  "totalPrice": {},
  "taxConditions": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/create-quotation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "voucherDate": "2026-05-07T12:00:00.000Z",
    "expirationDate": "2026-05-07T12:00:00.000Z",
    "address": {},
    "lineItems[]": [{}],
    "totalPrice": {},
    "taxConditions": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `voucherDate` | date | yes | RFC 3339 timestamp for the quotation date. |
| `expirationDate` | date | yes | RFC 3339 timestamp for the quotation expiration date. |
| `address` | object | yes | JSON object for the quotation recipient address. |
| `lineItems[]` | array<object> | yes | JSON array of quotation line item objects. |
| `totalPrice` | object | yes | JSON object for the quotation total price. |
| `taxConditions` | object | yes | JSON object describing quotation tax conditions. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `finalize` | boolean | no | Set to true to create an open quotation instead of the default draft quotation. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "resourceUri": "string",
      "updatedDate": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDate` | date |  |
| `id` | string |  |
| `resourceUri` | string |  |
| `updatedDate` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Lexware Office API, this operation is `POST /v1/quotations` (base URL `https://api.lexware.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-quotation.md) for the provider-specific parameters and requirements.

