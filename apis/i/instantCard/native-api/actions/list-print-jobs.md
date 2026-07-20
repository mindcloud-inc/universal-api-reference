# List Print Jobs with InstantCard

Retrieves a list of print jobs from InstantCard.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/organizations/:organizationId/print_jobs`
- **Base URL:** `https://core.instantcard.net`
- **Official documentation:** [List Print Jobs](https://instantcard.net/api/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | Organization ID from your InstantCard account. |
| `status` | query | `number` | no | Optional print job status filter: 0 for created jobs or 1 for submitted jobs. |
