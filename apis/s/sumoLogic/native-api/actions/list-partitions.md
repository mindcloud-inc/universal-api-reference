# List Partitions with Sumo Logic

Retrieves partitions from your Sumo Logic organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/partitions`
- **Base URL:** `https://api.sumologic.com/api`
- **Official documentation:** [List Partitions](https://api.sumologic.com/docs/#/partitionManagement/listPartitions)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `viewTypes[]` | query | `array<string>` | no | Partition view types to retrieve. Send multiple values as a array. |
