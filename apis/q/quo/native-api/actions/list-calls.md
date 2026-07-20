# List Calls with Quo

Retrieves all existing calls from Quo.

## Endpoint

- **Method:** `GET`
- **Path:** `/calls`
- **Base URL:** `https://api.openphone.com/v1`
- **Official documentation:** [List Calls](https://www.quo.com/docs/mdx/api-reference/calls/list-calls)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `createdAfter` | query | `date` | no |
| `createdBefore` | query | `date` | no |
| `participants[]` | query | `array<string>` | yes |
| `phoneNumberId` | query | `string` | yes |
| `userId` | query | `string` | no |
