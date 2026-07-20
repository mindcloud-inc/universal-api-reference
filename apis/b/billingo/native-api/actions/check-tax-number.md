# Check Tax Number with Billingo

Retrieves tax number validation details from Billingo.

## Endpoint

- **Method:** `GET`
- **Path:** `/utils/check-tax-number/:taxNumber`
- **Base URL:** `https://api.billingo.hu/v3`
- **Official documentation:** [Check Tax Number](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tax_number` | path | `string` | yes | Tax number to validate. |
