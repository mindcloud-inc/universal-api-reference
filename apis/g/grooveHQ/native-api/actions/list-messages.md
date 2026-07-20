# List Messages with GrooveHQ

Retrieves messages for a ticket in GrooveHQ.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets/:ticketNumber/messages`
- **Base URL:** `https://api.groovehq.com/v1`
- **Official documentation:** [List Messages](https://doc.groovehq.com/messages)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ticketNumber` | path | `string` | yes |
