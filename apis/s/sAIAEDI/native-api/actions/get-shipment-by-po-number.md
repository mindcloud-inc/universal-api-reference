# Get Shipment by PO Number with SAIA EDI

Retrieves a shipment from SAIA EDI by PO number.

## Endpoint

- **Method:** `POST`
- **Path:** `/webservice/shipment/xml.aspx`
- **Base URL:** `https://www.saiasecure.com`
- **Official documentation:** [Get Shipment by PO Number](https://www.saiasecure.com/webservice/shipment/n_GetByPONumber.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Api-Version` | `V1` |
| `Content-Type` | `text/xml` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PONumber` | body | `string` | yes | Customer purchase order number. |
| `OriginZipcode` | body | `string` | yes | Origin ZIP code for the shipment lookup. |
| `DestinationZipcode` | body | `string` | yes | Destination ZIP code for the shipment lookup. |
