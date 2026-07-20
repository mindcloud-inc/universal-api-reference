# Create Bill of Lading with SAIA EDI

Creates a bill of lading in SAIA EDI.

## Endpoint

- **Method:** `POST`
- **Path:** `/webservice/BOL/xml.aspx`
- **Base URL:** `https://www.saiasecure.com`
- **Official documentation:** [Create Bill of Lading](https://www.saiasecure.com/webservice/bol/Create.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Api-Version` | `V1` |
| `Content-Type` | `text/xml` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ShipmentDate` | body | `string` | yes | Shipment date in YYYY-MM-DD format. |
| `BillingTerms` | body | `string` | yes | Billing terms: Prepaid or Collect. |
| `PrintRates` | body | `string` | yes | Print rates flag: Y or N. |
| `Customs` | body | `string` | yes | Customs flag: Y or N. |
| `VICS` | body | `string` | yes | VICS standard bill of lading flag: Y or N. |
| `Shipper` | body | `object` | yes | Shipper object containing ContactName, Address1, City, State, and Zipcode. |
| `Consignee` | body | `object` | yes | Consignee object containing ContactName, Address1, City, State, and Zipcode. |
| `Details` | body | `object` | yes | Details object containing one or more DetailItem commodity entries. |
