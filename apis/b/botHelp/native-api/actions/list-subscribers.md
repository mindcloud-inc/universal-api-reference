# List Subscribers with BotHelp

Retrieves subscriber records from BotHelp.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/subscribers/`
- **Base URL:** `https://api.bothelp.io`
- **Official documentation:** [List Subscribers](https://main.bothelp.io/swagger)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `number` | no | Subscriber pagination cursor by ID. |
| `createdAtAfter` | query | `number` | no | Return subscribers created after this Unix timestamp. |
| `email` | query | `string` | no | Filter subscribers by email. |
| `phone` | query | `string` | no | Filter subscribers by phone. |
