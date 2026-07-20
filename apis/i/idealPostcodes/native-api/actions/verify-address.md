# Verify Address with Ideal Postcodes

Verifies and standardizes a US address in Ideal Postcodes.

## Endpoint

- **Method:** `POST`
- **Path:** `/verify/addresses`
- **Base URL:** `https://api.ideal-postcodes.co.uk/v1`
- **Official documentation:** [Verify Address](https://docs.ideal-postcodes.co.uk/docs/api/address-verify)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Address input to verify. |
| `zip_code` | body | `string` | no | ZIP code for the address. |
| `city` | body | `string` | no | City component for the address. |
| `state` | body | `string` | no | State abbreviation for the address. |
| `context` | query | `string` | no | Country context to use when verifying the address, for example USA. |
| `tags` | query | `string` | no | Comma-separated tags used to annotate the request context. |
