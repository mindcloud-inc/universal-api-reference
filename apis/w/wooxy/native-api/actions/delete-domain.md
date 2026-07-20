# Delete Domain with Wooxy

Deletes an existing domain from Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/domain/remove`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Delete Domain](https://wooxy.com/api-documentation/domains/remove-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | no | The registered domain name to delete. Preferred field based on runtime verification. |
| `domainId` | body | `string` | no | The Wooxy domain ID to delete. Use when you already have the ID. |
| `webHookUri` | body | `string` | no | Optional webhook URL to receive the completed domain deletion callback. |
