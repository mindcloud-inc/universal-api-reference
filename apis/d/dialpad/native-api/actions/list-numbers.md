# List Numbers with Dialpad

Retrieves company phone numbers from Dialpad.

## Endpoint

- **Method:** `GET`
- **Path:** `/numbers`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [List Numbers](https://developers.dialpad.com/reference/numberslist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Filter numbers by Dialpad status. |
| `cursor` | query | `string` | no | Pagination cursor from a previous Dialpad numbers response. |
