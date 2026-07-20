# Find Address with Data8

Finds addresses in Data8 by town or street.

## Endpoint

- **Method:** `POST`
- **Path:** `/AddressCapture/FindAddress.json`
- **Base URL:** `https://webservices.data-8.co.uk`
- **Official documentation:** [Find Address](https://docs.data-8.co.uk/web-services/addresscapture/findaddress)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `licence` | body | `string` | yes | The licence type under which you are accessing the service. |
| `town` | body | `string` | no | The name of the locality to search in. |
| `street` | body | `string` | no | The name of the street to search in. |
| `building` | body | `string` | no | The name or number of the address to search for. |
| `options` | body | `object` | no | Optional settings that control address retrieval behavior. |
