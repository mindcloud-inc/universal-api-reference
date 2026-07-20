# Lookup Carrier with Lookify

## Endpoint

- **Method:** `POST`
- **Path:** `/api/enterprise/carrier`
- **Base URL:** `https://lookify.io`
- **Official documentation:** [Lookup Carrier](https://lookify.io/assets/pdfs/enterprise_carrier_api_documentation.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nid` | body | `string` | yes | The phone number to search. |
| `country` | body | `string` | no | Optional country for the phone number search. |
