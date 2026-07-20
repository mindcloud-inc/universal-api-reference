# Create Pickup Request with SAIA EDI

Creates a pickup request in SAIA EDI.

## Endpoint

- **Method:** `POST`
- **Path:** `/webservice/pickup/xml.aspx`
- **Base URL:** `https://www.saiasecure.com`
- **Official documentation:** [Create Pickup Request](https://www.saiasecure.com/webservice/pickup/Create.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Api-Version` | `V1` |
| `Content-Type` | `text/xml` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AccountNumber` | body | `string` | yes | Saia account number for pickup. |
| `PickupDate` | body | `string` | yes | Pickup date in YYYY-MM-DD format. |
| `ReadyTime` | body | `string` | yes | Ready time in HH:MM:SS format. |
| `CloseTime` | body | `string` | yes | Close time in HH:MM:SS format. |
| `TotalPieces` | body | `string` | yes | Total pieces for pickup. |
| `TotalWeight` | body | `string` | yes | Total shipment weight. |
| `CompanyName` | body | `string` | no | Pickup location company name. |
| `Street` | body | `string` | no | Pickup street address. |
| `City` | body | `string` | no | Pickup city. |
| `State` | body | `string` | no | Pickup state abbreviation. |
| `Zipcode` | body | `string` | no | Pickup ZIP code. |
