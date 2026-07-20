# Find Whois with Clearout

Retrieves Whois records for a domain from Clearout.

## Endpoint

- **Method:** `POST`
- **Path:** `/domain/resolve/whois`
- **Base URL:** `https://api.clearout.io/v2`
- **Official documentation:** [Find Whois](https://docs.clearout.io/developers/api/misc-domain-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | Find Whois record for domain |
| `timeout` | body | `number` | no | Request wait time (in milliseconds), Maximum allowed wait time should not exceed 110000 milliseconds |
