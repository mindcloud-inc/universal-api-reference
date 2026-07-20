# List Signals with Das Keyboard 5Q

Retrieves signals from Das Keyboard 5Q.

## Endpoint

- **Method:** `GET`
- **Path:** `/signals`
- **Base URL:** `https://q2.daskeyboard.com/api/1.0`
- **Official documentation:** [List Signals](https://www.daskeyboard.io/api-ressources/signal/get-signals/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sort` | query | `string` | no | Sort expression for signals. The docs show createdAt,DESC or createdAt,ASC. |
