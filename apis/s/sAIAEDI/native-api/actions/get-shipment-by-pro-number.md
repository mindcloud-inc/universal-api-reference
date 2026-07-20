# Get Shipment by PRO Number with SAIA EDI

Retrieves a shipment from SAIA EDI by PRO number.

## Endpoint

- **Method:** `POST`
- **Path:** `/webservice/shipment/xml.aspx`
- **Base URL:** `https://www.saiasecure.com`
- **Official documentation:** [Get Shipment by PRO Number](https://www.saiasecure.com/webservice/shipment/n_GetByProNumber.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Api-Version` | `V1` |
| `Content-Type` | `text/xml` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProNumber` | body | `string` | yes | Saia PRO number to trace. |
