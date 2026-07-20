# List Ticket Messages with HelpSpace

Retrieves messages for a HelpSpace ticket.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/{id}/messages`
- **Base URL:** `https://api.helpspace.com/api/v1`
- **Official documentation:** [List Ticket Messages](https://documentation.helpspace.com/api-message)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | HelpSpace ticket identifier. |
