# List Job History with Gladia

Retrieves historical job records from Gladia.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/history`
- **Base URL:** `https://api.gladia.io`
- **Official documentation:** [List Job History](https://api.gladia.io/openapi.json)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `date` | no | — |
| `before_date` | query | `date` | no | — |
| `after_date` | query | `date` | no | — |
| `status` | query | `list<string>` | no | Accepted values: `done`, `error`, `processing`, `queued`. |
| `kind` | query | `list<string>` | no | Accepted values: `live`, `pre-recorded`. |
