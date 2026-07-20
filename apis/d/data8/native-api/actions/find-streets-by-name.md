# Find Streets by Name with Data8

Finds streets in Data8 by locality name.

## Endpoint

- **Method:** `POST`
- **Path:** `/AddressCapture/StreetsByName.json`
- **Base URL:** `https://webservices.data-8.co.uk`
- **Official documentation:** [Find Streets by Name](https://docs.data-8.co.uk/web-services/addresscapture/streetsbyname)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `licence` | body | `string` | yes | The licence type under which you are accessing the service. |
| `locality` | body | `string` | no | The name of the locality to search in. |
| `street` | body | `string` | no | The name of the street to search for. |
| `options` | body | `object` | no | Optional settings that control address retrieval behavior. |
