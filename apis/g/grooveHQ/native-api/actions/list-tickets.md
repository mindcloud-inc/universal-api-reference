# List Tickets with GrooveHQ

Retrieves tickets from GrooveHQ.

## Endpoint

- **Method:** `GET`
- **Path:** `/tickets`
- **Base URL:** `https://api.groovehq.com/v1`
- **Official documentation:** [List Tickets](https://doc.groovehq.com/tickets)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `assignee` | query | `string` | no |
| `customer` | query | `string` | no |
| `state` | query | `string` | no |
| `folder` | query | `string` | no |
