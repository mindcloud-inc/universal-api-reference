# Key Lookup with Precisely

Retrieves an address from Precisely by PreciselyID or EIR code.

## Endpoint

- **Method:** `GET`
- **Path:** `/geocode/v1/keylookup`
- **Base URL:** `https://api.precisely.com`
- **Official documentation:** [Key Lookup](https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/Geocode/key_lookup_get_request.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | query | `string` | yes | Precisely geocode key value to look up. |
| `type` | query | `string` | yes | Key type, for example PB_KEY. |
| `country` | query | `string` | no | ISO country code or country name. |
| `objectId` | query | `number` | no | Optional object identifier for the lookup request. |
