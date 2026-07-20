# Verify Domain with Wooxy

Verifies an existing domain in Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/domain/verify`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Verify Domain](https://wooxy.com/api-documentation/domains/verify-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domainId` | body | `string` | no | The Wooxy domain ID. Use this or Domain. |
| `domain` | body | `string` | no | The registered domain name. Use this or Domain ID. |
