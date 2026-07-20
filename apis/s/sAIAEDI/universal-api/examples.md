# SAIA EDI Universal API Examples

These examples use the MindCloud API key and SAIA EDI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Shipment by PRO Number

Retrieves a shipment from SAIA EDI by PRO number.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAIAEDI/latest/actions/get-shipment-by-pro-number?connectionId=$CONNECTION_ID&ProNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ProNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sAIAEDI/latest/actions/get-shipment-by-pro-number?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "Accessorials": "string",
      "ActualDeliveryDays": 1,
      "Appointment": "string",
      "BillingTerms": "string",
      "BLNumber": "string",
      "CargoControlNumber": "string",
      "CODAmount": 1,
      "Code": "string",
      "Consignee": {},
      "CurrentStatus": "string",
      "DeliveryAppointmentDateTime": "string",
      "DeliveryDateTime": "string",
      "DeliveryDateTimeArrive": "string",
      "DeliveryDateTimeDepart": "string",
      "DestinationTerminal": "string",
      "Details": {},
      "DiscountAmount": 1,
      "DriverNumber": "string",
      "Element": "string",
      "ExpectedDeliveryDate": "string",
      "Fault": "string",
      "FreightCharges": 1,
      "FromPartner": {},
      "Hazardous": "string",
      "History": {},
      "LatePickup": "string",
      "MailTo": "string",
      "MasterProNumber": "string",
      "Message": "string",
      "NetCharges": 1,
      "OnTime": "string",
      "OriginTerminal": "string",
      "PickupDateTime": "string",
      "Pieces": 1,
      "PONumber": "string",
      "ProNumber": "string",
      "Rates": {},
      "ReferenceNumber": "string",
      "Shipper": {},
      "ShipperNumber": "string",
      "ShippingWeight": 1,
      "Signature": "string",
      "StandardServiceDays": 1,
      "Tariff": "string",
      "TestMode": "string",
      "ThirdParty": {},
      "ToPartner": {},
      "TrailerNumber": "string",
      "WeightedAverageFreightClass": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Shipment by PRO Number action reference](actions/get-shipment-by-pro-number.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sAIAEDI/latest/actions/get-shipment-by-pro-number).

## Create Bill of Lading

Creates a bill of lading in SAIA EDI.

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

Example response:

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

See the full [Create Bill of Lading action reference](actions/create-bill-of-lading.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sAIAEDI/latest/actions/create-bill-of-lading).
