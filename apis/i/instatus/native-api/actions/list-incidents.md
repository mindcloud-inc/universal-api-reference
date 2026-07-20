# List Incidents with Instatus

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:page_id/incidents`
- **Base URL:** `https://api.instatus.com`
- **Official documentation:** [List Incidents](https://instatus.com/help/api/incidents)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_id` | path | `string` | yes | Instatus status page ID. |
