# List MID Requests with Fidel API

Retrieves MID requests from a Fidel program.

## Endpoint

- **Method:** `GET`
- **Path:** `/programs/:programId/mid-requests`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [List MID Requests](https://reference.fidel.uk/reference/list-mid-requests)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `programId` | path | `string` | yes |
