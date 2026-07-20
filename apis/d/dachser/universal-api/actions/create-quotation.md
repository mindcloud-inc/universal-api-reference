# Dachser: Create Quotation

Creates a new quotation in Dachser.

```
POST https://connect.mindcloud.co/v1/universal/dachser/latest/actions/create-quotation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dachser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dachser/latest/actions/create-quotation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transportOrder": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dachser/latest/actions/create-quotation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transportOrder": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `logisticsType` | string | no | D for distribution or P for procurement. Default: `D`. |
| `saveQuotation` | boolean | no | Whether to save the quotation in eLogistics. Default: `false`. |
| `transportOrder` | object | yes | Transport data for the quotation price calculation. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `acceptLanguage` | string | no | Optional language sent as the Accept-Language header. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "quotationDate": "2026-05-07T12:00:00.000Z",
      "quotationDetails": [
        {}
      ],
      "remarks": [
        "string"
      ],
      "totalAmount": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `quotationDate` | date |  |
| `quotationDetails` | array<object> |  |
| `remarks` | array<string> |  |
| `totalAmount` | object |  |

## Native endpoint

Through the native Dachser API, this operation is `POST /rest/v2/quotations` (base URL `https://api-gateway.dachser.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-quotation.md) for the provider-specific parameters and requirements.

