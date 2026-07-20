# Get Notebook with Datadog

Retrieves a notebook from Datadog.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/notebooks/:notebook_id`
- **Base URL:** `https://api.us5.datadoghq.com`
- **Official documentation:** [Get Notebook](https://docs.datadoghq.com/api/latest/notebooks/#get-a-notebook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `notebook_id` | path | `number` | yes | Unique notebook ID. |
