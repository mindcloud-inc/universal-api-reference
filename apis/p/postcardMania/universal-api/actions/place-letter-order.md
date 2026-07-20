# PostcardMania: Place Letter Order

Creates a new letter order in PostcardMania.

```
POST https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/place-letter-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostcardMania `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/place-letter-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "envelope": {
    "type": "Regular"
  },
  "mailClass": "FirstClass",
  "color": "false",
  "printOnBothSides": "false",
  "insertAddressingPage": "false",
  "recipients[]": [
    {
      "city": "Clearwater",
      "state": "FL",
      "address": "123 Main St",
      "zipCode": "33756",
      "lastName": "User",
      "firstName": "Test"
    }
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/place-letter-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "envelope": {"type":"Regular"},
    "mailClass": "FirstClass",
    "color": "false",
    "printOnBothSides": "false",
    "insertAddressingPage": "false",
    "recipients[]": [{"city":"Clearwater","state":"FL","address":"123 Main St","zipCode":"33756","lastName":"User","firstName":"Test"}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `designID` | string | no | Existing approved design to use for the letter order. |
| `letter` | string | no | Raw HTML letter content when not using a design ID. Default: `<p>Hello</p>`. |
| `envelope` | object | yes | Envelope object required for letter orders. Default: `{"type":"Regular"}`. |
| `mailClass` | string | yes | Mail class for the order. Default: `FirstClass`. |
| `color` | boolean | yes | Whether the letter should print in color. Default: `false`. |
| `printOnBothSides` | boolean | yes | Whether to print on both sides. Default: `false`. |
| `insertAddressingPage` | boolean | yes | Whether to insert an addressing page. Default: `false`. |
| `recipients[]` | array<object> | yes | Recipient list for the order. Default: `[{"city":"Clearwater","state":"FL","address":"123 Main St","zipCode":"33756","lastName":"User","firstName":"Test"}]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchID": 1,
      "extRefNbr": "string",
      "orderID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchID` | number | Created batch identifier. |
| `extRefNbr` | string | External reference number when provided. |
| `orderID` | number | Created order identifier. |

## Native endpoint

Through the native PostcardMania API, this operation is `POST /order/letter` (base URL `https://v3.pcmintegrations.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/place-letter-order.md) for the provider-specific parameters and requirements.

