# Get webhooks for the team with Digital Samba

Retrieves team webhooks from Digital Samba.

## Endpoint

- **Method:** `GET`
- **Path:** `/webhooks`
- **Base URL:** `https://api.digitalsamba.com/api/v1`
- **Official documentation:** [Get webhooks for the team](https://developer.digitalsamba.com/rest-api/#webhooks-GETapi-v1-webhooks)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | The UUID of the webhook after which records will be returned. |
