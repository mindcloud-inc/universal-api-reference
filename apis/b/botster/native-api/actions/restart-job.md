# Restart Job with Botster

Restarts an existing job in Botster.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs/:jobId/restart`
- **Base URL:** `https://botster.io/api/v2`
- **Official documentation:** [Restart Job](https://botster.io/info/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | The Botster job UUID. |
