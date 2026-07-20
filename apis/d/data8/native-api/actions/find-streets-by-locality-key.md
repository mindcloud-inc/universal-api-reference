# Find Streets by Locality Key with Data8

Finds streets in Data8 by locality key.

## Endpoint

- **Method:** `POST`
- **Path:** `/AddressCapture/StreetsByLocalityKey.json`
- **Base URL:** `https://webservices.data-8.co.uk`
- **Official documentation:** [Find Streets by Locality Key](https://docs.data-8.co.uk/web-services/addresscapture/streetsbylocalitykey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `licence` | body | `string` | yes | The licence type under which you are accessing the service. |
| `localityKey` | body | `string` | yes | The unique identifier of the locality to search in. |
| `street` | body | `string` | no | The name of the street to search for. |
| `options` | body | `object` | no | Optional settings that control address retrieval behavior. |
