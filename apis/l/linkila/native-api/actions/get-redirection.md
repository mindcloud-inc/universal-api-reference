# Get Redirection with Linkila

Retrieves a destination URL from Linkila and logs access.

## Endpoint

- **Method:** `POST`
- **Path:** `/redirection`
- **Base URL:** `https://app.linkila.com/integrations/api/v1`
- **Official documentation:** [Get Redirection](https://app.linkila.com/integrations/api/v1/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shortURL` | body | `string` | no | Short URL to resolve. Provide either Short URL or Link ID. |
| `linkId` | body | `string` | no | Link ID to resolve. Provide either Short URL or Link ID. |
| `ip` | body | `string` | no | Optional request IP address context for redirection resolution. |
| `headers` | body | `object` | no | Optional request headers object for redirection resolution. |
