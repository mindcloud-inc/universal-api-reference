# SAIA EDI: Create Bill of Lading

Creates a bill of lading in SAIA EDI.

```
POST https://connect.mindcloud.co/v1/universal/sAIAEDI/latest/actions/create-bill-of-lading
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SAIA EDI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sAIAEDI/latest/actions/create-bill-of-lading" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ShipmentDate": "string",
  "BillingTerms": "string",
  "PrintRates": "string",
  "Customs": "string",
  "VICS": "string",
  "Shipper": {},
  "Consignee": {},
  "Details": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sAIAEDI/latest/actions/create-bill-of-lading', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ShipmentDate": "string",
    "BillingTerms": "string",
    "PrintRates": "string",
    "Customs": "string",
    "VICS": "string",
    "Shipper": {},
    "Consignee": {},
    "Details": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ShipmentDate` | string | yes | Shipment date in YYYY-MM-DD format. |
| `BillingTerms` | string | yes | Billing terms: Prepaid or Collect. |
| `PrintRates` | string | yes | Print rates flag: Y or N. |
| `Customs` | string | yes | Customs flag: Y or N. |
| `VICS` | string | yes | VICS standard bill of lading flag: Y or N. |
| `Shipper` | object | yes | Shipper object containing ContactName, Address1, City, State, and Zipcode. |
| `Consignee` | object | yes | Consignee object containing ContactName, Address1, City, State, and Zipcode. |
| `Details` | object | yes | Details object containing one or more DetailItem commodity entries. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Barcode": "string",
      "CheckDigit": "string",
      "Code": "string",
      "Element": "string",
      "Fault": "string",
      "HTML": "string",
      "Message": "string",
      "PDF": "string",
      "ProNumber": "string",
      "TestMode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Barcode` | string | Barcode value or payload when returned. |
| `CheckDigit` | string | Check digit for the returned PRO number. |
| `Code` | string | Saia error code; blank indicates no documented error. |
| `Element` | string | Element associated with an error when available. |
| `Fault` | string | Fault classification returned by Saia. |
| `HTML` | string | HTML document payload when returned. |
| `Message` | string | Error or status message. |
| `PDF` | string | PDF document payload or URL when returned. |
| `ProNumber` | string | Created bill-of-lading PRO number when returned. |
| `TestMode` | string | Y or N test-mode flag echoed by Saia. |

## Native endpoint

Through the native SAIA EDI API, this operation is `POST /webservice/BOL/xml.aspx` (base URL `https://www.saiasecure.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bill-of-lading.md) for the provider-specific parameters and requirements.

