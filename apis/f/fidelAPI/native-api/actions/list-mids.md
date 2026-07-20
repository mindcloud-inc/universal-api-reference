# List MIDs with Fidel API

Retrieves MIDs from a Fidel program.

## Endpoint

- **Method:** `GET`
- **Path:** `/programs/:programId/mids`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [List MIDs](https://reference.fidel.uk/reference/list-mids)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `programId` | path | `string` | yes |
