# List Sync Runs with Hightouch

Retrieves sync runs from Hightouch.

## Endpoint

- **Method:** `GET`
- **Path:** `/syncs/{syncId}/runs`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [List Sync Runs](https://api.hightouch.io/api/swagger.json)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `syncId` | path | `number` | yes | The sync ID. |
| `runId` | query | `number` | no | Query for a specific sync run ID. |
| `after` | query | `date` | no | Select sync runs started after this ISO timestamp. |
| `before` | query | `date` | no | Select sync runs started before this ISO timestamp. |
| `within` | query | `number` | no | Select sync runs started within the last given number of minutes. |
