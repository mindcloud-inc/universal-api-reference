# Update Domain Details with GoDaddy CRM

Updates a domain's details in GoDaddy.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/domains/:domain`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Update Domain Details](https://developer.godaddy.com/doc/endpoint/domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | Required domain whose details should be updated |
| `renewAuto` | body | `boolean` | no | Whether the domain should renew automatically |
