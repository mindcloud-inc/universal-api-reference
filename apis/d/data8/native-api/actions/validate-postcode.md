# Validate Postcode with Data8

Validates a submitted postcode with Data8.

## Endpoint

- **Method:** `POST`
- **Path:** `/AddressCapture/ValidatePostcode.json`
- **Base URL:** `https://webservices.data-8.co.uk`
- **Official documentation:** [Validate Postcode](https://docs.data-8.co.uk/web-services/addresscapture/validatepostcode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `licence` | body | `string` | yes | The licence type under which you are accessing the service. |
| `postcode` | body | `string` | yes | The postcode to validate. |
| `options` | body | `object` | no | Optional settings that control address retrieval behavior. |
