# List Memory Jobs with CrewMem

## Endpoint

- **Method:** `GET`
- **Path:** `/api/memory/jobs`
- **Base URL:** `https://crewmem.com`
- **Official documentation:** [List Memory Jobs](https://crewmem.com/docs/api/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Number of jobs to return |
| `offset` | query | `number` | no | Offset for pagination |
