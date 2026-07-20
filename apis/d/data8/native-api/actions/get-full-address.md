# Get Full Address with Data8

Retrieves a full address from Data8 by postcode.

## Endpoint

- **Method:** `POST`
- **Path:** `/AddressCapture/GetFullAddress.json`
- **Base URL:** `https://webservices.data-8.co.uk`
- **Official documentation:** [Get Full Address](https://docs.data-8.co.uk/web-services/addresscapture/getfulladdress)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `licence` | body | `string` | yes | The licence type under which you are accessing the service. |
| `postcode` | body | `string` | yes | The full postcode to search for. |
| `building` | body | `string` | no | The optional name or number of the address to search for. |
| `options` | body | `object` | no | Optional settings that control address retrieval behavior. |
