# Retrieve Address with Address Auto-Complete by Fetchify

Retrieves a full address from Fetchify by address ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/retrieve`
- **Base URL:** `https://api.craftyclicks.co.uk/address/1.1`
- **Official documentation:** [Retrieve Address](https://docs.fetchify.com/json-api/address-auto-complete.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | The address identifier returned by Find Addresses. |
| `country` | query | `string` | yes | Three-letter Fetchify country code such as `gbr` or `usa`. |
| `extra.gbr_ceremonial_counties` | query | `boolean` | no | When enabled, return ceremonial counties for Great Britain addresses. |
