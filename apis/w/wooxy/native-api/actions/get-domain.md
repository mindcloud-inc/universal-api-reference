# Get Domain with Wooxy

Retrieves a domain from your Wooxy account.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/domain/get`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Get Domain](https://wooxy.com/api-documentation/domains/get-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domainId` | body | `string` | no | The Wooxy domain ID. Use this or Domain. |
| `domain` | body | `string` | no | The registered domain name. Use this or Domain ID. |
