# Fetch Address with Data8

Retrieves an address from Data8 by address key.

## Endpoint

- **Method:** `POST`
- **Path:** `/AddressCapture/FetchAddress.json`
- **Base URL:** `https://webservices.data-8.co.uk`
- **Official documentation:** [Fetch Address](https://docs.data-8.co.uk/web-services/addresscapture/fetchaddress)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `licence` | body | `string` | yes | The licence type under which you are accessing the service. |
| `addressKey` | body | `string` | yes | The unique identifier of the address to retrieve. |
| `options` | body | `object` | no | Optional settings that control address retrieval behavior. |
