# Find Localities by Postcode with Data8

Finds localities in Data8 by postcode.

## Endpoint

- **Method:** `POST`
- **Path:** `/AddressCapture/LocalitiesByPostcode.json`
- **Base URL:** `https://webservices.data-8.co.uk`
- **Official documentation:** [Find Localities by Postcode](https://docs.data-8.co.uk/web-services/addresscapture/localitiesbypostcode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `licence` | body | `string` | yes | The licence type under which you are accessing the service. |
| `postcode` | body | `string` | yes | The full or partial postcode to search for. |
| `options` | body | `object` | no | Optional settings that control address retrieval behavior. |
