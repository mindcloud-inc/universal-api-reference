# Get Address Details with Byteplant Address Validator

Retrieves address details from Byteplant Address Validator by suggestion ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/fetch`
- **Base URL:** `https://api.address-validator.net`
- **Official documentation:** [Get Address Details](https://www.byteplant.com/address-validator/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ID` | query | `string` | yes | Address id returned by Search Address Suggestions. |
| `Geocoding` | query | `boolean` | no | Include latitude and longitude in the response. |
| `Timeout` | query | `number` | no | Request timeout in seconds. |
