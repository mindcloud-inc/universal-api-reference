# Get analytics with Bulldog-WP

Retrieves analytics from Bulldog-WP.

## Endpoint

- **Method:** `GET`
- **Path:** `/analytics`
- **Base URL:** `https://api.bulldog-wp.co.il/v1`
- **Official documentation:** [Get analytics](https://console.bulldog-wp.co.il/docs/specification)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `date` | yes | Start date in ISO 8601 format. |
| `to` | query | `date` | yes | End date in ISO 8601 format. |
| `devices` | query | `string<string>` | yes | One or more WhatsApp device IDs. Required by the live API for analytics requests. Send multiple values as a string separated by `,`. |
