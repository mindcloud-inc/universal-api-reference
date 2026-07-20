# Get IBAN Lookup with Greip - Fraud Prevention

Retrieves IBAN lookup data from Greip.

## Endpoint

- **Method:** `GET`
- **Path:** `/lookup/iban`
- **Base URL:** `https://greipapi.com`
- **Official documentation:** [Get IBAN Lookup](https://docs.greip.io/api-reference/endpoint/data-lookup/iban)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `iban` | query | `string` | yes | The IBAN value to validate and enrich. |
