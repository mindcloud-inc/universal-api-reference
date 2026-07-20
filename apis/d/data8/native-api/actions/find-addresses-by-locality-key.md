# Find Addresses by Locality Key with Data8

Finds addresses in Data8 by locality key.

## Endpoint

- **Method:** `POST`
- **Path:** `/AddressCapture/AddressesByLocalityKey.json`
- **Base URL:** `https://webservices.data-8.co.uk`
- **Official documentation:** [Find Addresses by Locality Key](https://docs.data-8.co.uk/web-services/addresscapture/addressesbylocalitykey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `licence` | body | `string` | yes | The licence type under which you are accessing the service. |
| `localityKey` | body | `string` | yes | The unique identifier of the locality to search in. |
| `building` | body | `string` | no | The name or number of the address to search for. |
| `options` | body | `object` | no | Optional settings that control address retrieval behavior. |
