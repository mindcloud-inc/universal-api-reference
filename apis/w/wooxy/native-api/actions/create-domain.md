# Create Domain with Wooxy

Creates a new domain in Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/domain/create`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Create Domain](https://wooxy.com/api-documentation/domains/create-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | The domain to create. Must be a valid domain name. |
| `webHookUri` | body | `string` | no | Optional webhook URL to receive the domain-created callback. |
