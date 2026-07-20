# SAIA EDI: Get Shipment by PO Number

Retrieves a shipment from SAIA EDI by PO number.

```
GET https://connect.mindcloud.co/v1/universal/sAIAEDI/latest/actions/get-shipment-by-po-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SAIA EDI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAIAEDI/latest/actions/get-shipment-by-po-number?connectionId=$CONNECTION_ID&PONumber=string&OriginZipcode=string&DestinationZipcode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "PONumber": "string",
  "OriginZipcode": "string",
  "DestinationZipcode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sAIAEDI/latest/actions/get-shipment-by-po-number?${params}`, {
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
| `PONumber` | string | yes | Customer purchase order number. |
| `OriginZipcode` | string | yes | Origin ZIP code for the shipment lookup. |
| `DestinationZipcode` | string | yes | Destination ZIP code for the shipment lookup. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Accessorials` | string | Accessorial indicator or details. |
| `ActualDeliveryDays` | number | Actual delivery days. |
| `Appointment` | string | Appointment indicator. |
| `BillingTerms` | string | Billing terms. |
| `BLNumber` | string | Bill of lading number. |
| `CargoControlNumber` | string | Cargo control number. |
| `CODAmount` | number | COD amount. |
| `Code` | string | Saia error code; blank indicates no documented error. |
| `Consignee` | object | Consignee account and address details. |
| `CurrentStatus` | string | Current shipment status. |
| `DeliveryAppointmentDateTime` | string | Scheduled delivery appointment date/time. |
| `DeliveryDateTime` | string | Delivery date/time. |
| `DeliveryDateTimeArrive` | string | Delivery arrival date/time. |
| `DeliveryDateTimeDepart` | string | Delivery departure date/time. |
| `DestinationTerminal` | string | Destination terminal. |
| `Details` | object | Shipment detail lines when returned. |
| `DiscountAmount` | number | Discount amount. |
| `DriverNumber` | string | Driver number when returned. |
| `Element` | string | Element associated with an error when available. |
| `ExpectedDeliveryDate` | string | Expected delivery date. |
| `Fault` | string | Fault classification returned by Saia. |
| `FreightCharges` | number | Freight charges. |
| `FromPartner` | object | Origin EDI partner details. |
| `Hazardous` | string | Hazardous-material indicator. |
| `History` | object | Shipment history entries when returned. |
| `LatePickup` | string | Late pickup indicator when returned. |
| `MailTo` | string | Mail-to value when returned. |
| `MasterProNumber` | string | Master PRO number when applicable. |
| `Message` | string | Error or status message. |
| `NetCharges` | number | Net charges. |
| `OnTime` | string | On-time indicator when returned. |
| `OriginTerminal` | string | Origin terminal. |
| `PickupDateTime` | string | Pickup date/time. |
| `Pieces` | number | Piece count. |
| `PONumber` | string | Purchase order number. |
| `ProNumber` | string | Saia PRO number. |
| `Rates` | object | Rate details when returned. |
| `ReferenceNumber` | string | Additional shipment reference number. |
| `Shipper` | object | Shipper account and address details. |
| `ShipperNumber` | string | Shipper reference number. |
| `ShippingWeight` | number | Shipment weight. |
| `Signature` | string | Delivery signature. |
| `StandardServiceDays` | number | Standard service days. |
| `Tariff` | string | Tariff value. |
| `TestMode` | string | Y or N test-mode flag echoed by Saia. |
| `ThirdParty` | object | Third-party billing account and address details. |
| `ToPartner` | object | Destination EDI partner details. |
| `TrailerNumber` | string | Trailer number when returned. |
| `WeightedAverageFreightClass` | number | Weighted average freight class. |

## Native endpoint

Through the native SAIA EDI API, this operation is `POST /webservice/shipment/xml.aspx` (base URL `https://www.saiasecure.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipment-by-po-number.md) for the provider-specific parameters and requirements.

