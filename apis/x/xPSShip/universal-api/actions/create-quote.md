# XPS Ship: Create Quote

Creates a shipping quote in XPS Ship.

```
POST https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/create-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XPS Ship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/create-quote" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "senderCountry": "string",
  "senderZip": "string",
  "receiverCountry": "string",
  "receiverZip": "string",
  "weightUnit": "string",
  "dimUnit": "string",
  "currency": "string",
  "customsCurrency": "string",
  "pieces": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/create-quote', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "senderCountry": "string",
    "senderZip": "string",
    "receiverCountry": "string",
    "receiverZip": "string",
    "weightUnit": "string",
    "dimUnit": "string",
    "currency": "string",
    "customsCurrency": "string",
    "pieces": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `senderCountry` | string | yes | ISO two-character sender country code. |
| `senderZip` | string | yes | Sender ZIP or postal code. |
| `receiverCountry` | string | yes | ISO two-character receiver country code. |
| `receiverZip` | string | yes | Receiver ZIP or postal code. |
| `weightUnit` | string | yes | Weight unit: lb, oz, kg, or g. |
| `dimUnit` | string | yes | Dimension unit: in, cm, or null when package type has preset dimensions. |
| `currency` | string | yes | Currency for insurance, declared value, and customs value. |
| `customsCurrency` | string | yes | Currency for customs value. |
| `pieces` | list<object> | yes | Shipment pieces with weight, dimensions, insurance amount, and declared value. Accepts multiple values as an array. |
| `carrierCode` | string | no | Optional carrier code to limit the quote request. |
| `serviceCode` | string | no | Optional service code for quoting a specific service. |
| `packageTypeCode` | string | no | Optional package type code for quoting a specific package type. |
| `receiverCity` | string | no | Optional destination city or town. |
| `receiverEmail` | string | no | Optional receiver email address. |
| `residential` | boolean | no | Set true when the destination address is residential. |
| `signatureOptionCode` | string | no | Optional signature option code for the shipment. |
| `uspsExpressAmDelivery` | boolean | no | Optional USPS 10:30 AM delivery flag. |
| `saturdayDelivery` | boolean | no | Optional Saturday delivery flag. |
| `contentType` | string | no | Optional carrier-specific content type. |
| `contentDescription` | string | no | Optional shipment content description, often needed for international shipments. |
| `billingParty` | string | no | Optional billing party: sender, receiver, or third_party. |
| `providerAccountId` | string | no | Optional provider account ID for the quote request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseAmount": "string",
      "carrierCode": "string",
      "currency": "string",
      "customsCurrency": "string",
      "packageTypeCode": "string",
      "pieces": [
        {}
      ],
      "quotedWeight": "string",
      "quotedWeightType": "string",
      "quotes": [
        {}
      ],
      "serviceCode": "string",
      "serviceDescription": "string",
      "surcharges": [
        {}
      ],
      "totalAmount": "string",
      "zone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseAmount` | string | Base quoted amount. |
| `carrierCode` | string | Carrier code for the quote. |
| `currency` | string | Quote currency. |
| `customsCurrency` | string | Customs currency when returned. |
| `packageTypeCode` | string | Package type code for the quote. |
| `pieces` | array<object> | USPS multipiece quote details, when returned. |
| `quotedWeight` | string | Quoted weight amount. |
| `quotedWeightType` | string | Quoted weight type. |
| `quotes` | array<object> | Multiple quote results when no specific service or package type is specified. |
| `serviceCode` | string | Service code for the quote. |
| `serviceDescription` | string | Service description, returned when quoting multiple services. |
| `surcharges` | array<object> | Surcharges included in the quote. |
| `totalAmount` | string | Total quoted amount. |
| `zone` | string | Zone used to compute the quote. |

## Native endpoint

Through the native XPS Ship API, this operation is `POST /restapi/v1/customers/:customerId/quote` (base URL `https://xpsshipper.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-quote.md) for the provider-specific parameters and requirements.

