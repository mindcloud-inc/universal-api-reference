# Find MX Records with Clearout

Retrieves MX records for a domain from Clearout.

## Endpoint

- **Method:** `POST`
- **Path:** `/domain/resolve/mx`
- **Base URL:** `https://api.clearout.io/v2`
- **Official documentation:** [Find MX Records](https://docs.clearout.io/developers/api/misc-domain-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | Find MX records for domain |
| `timeout` | body | `number` | no | Request wait time (in milliseconds), Maximum allowed wait time should not exceed 110000 milliseconds |
