# Request Number Lookup with Mocean API

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/2/nl?mocean-resp-format=json`
- **Base URL:** `https://rest.moceanapi.com`
- **Official documentation:** [Request Number Lookup](https://moceanapi.com/docs#request-number-lookup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mocean-to` | query | `string` | yes | The phone number to look up, including country code. |
