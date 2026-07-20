# Find Localities by Name with Data8

Finds localities in Data8 by name.

## Endpoint

- **Method:** `POST`
- **Path:** `/AddressCapture/LocalitiesByName.json`
- **Base URL:** `https://webservices.data-8.co.uk`
- **Official documentation:** [Find Localities by Name](https://docs.data-8.co.uk/web-services/addresscapture/localitiesbyname)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `licence` | body | `string` | yes | The licence type under which you are accessing the service. |
| `name` | body | `string` | yes | The name of the locality to search for. |
| `options` | body | `object` | no | Optional settings that control address retrieval behavior. |
