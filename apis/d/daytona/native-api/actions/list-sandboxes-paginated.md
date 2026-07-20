# List Sandboxes Paginated with Daytona

Retrieves a paginated list of sandboxes from Daytona.

## Endpoint

- **Method:** `GET`
- **Path:** `/sandbox/paginated`
- **Base URL:** `https://app.daytona.io/api`
- **Official documentation:** [List Sandboxes Paginated](https://www.daytona.io/docs/tools/api/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Filter by partial sandbox ID match. |
| `name` | query | `string` | no | Filter by partial sandbox name match. |
| `labels` | query | `string` | no | JSON encoded labels to filter by. |
| `includeErroredDeleted` | query | `boolean` | no | Include results with errored state and deleted desired state. |
| `states[]` | query | `array<string>` | no | List of states to filter by. |
| `snapshots[]` | query | `array<string>` | no | List of snapshot names to filter by. |
| `regions[]` | query | `array<string>` | no | List of regions to filter by. |
| `minCpu` | query | `number` | no | Minimum CPU. |
| `maxCpu` | query | `number` | no | Maximum CPU. |
| `minMemoryGiB` | query | `number` | no | Minimum memory in GiB. |
| `maxMemoryGiB` | query | `number` | no | Maximum memory in GiB. |
| `minDiskGiB` | query | `number` | no | Minimum disk space in GiB. |
| `maxDiskGiB` | query | `number` | no | Maximum disk space in GiB. |
| `lastEventAfter` | query | `date` | no | Include items with last event after this timestamp. |
| `lastEventBefore` | query | `date` | no | Include items with last event before this timestamp. |
