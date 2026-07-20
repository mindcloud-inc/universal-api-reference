# Get Activation Run with Checkmk

Retrieves activation run details from Checkmk.

## Endpoint

- **Method:** `GET`
- **Path:** `/objects/activation_run/{activation_id}`
- **Base URL:** `{apiUrl}`
- **Official documentation:** [Get Activation Run](https://docs.checkmk.com/latest/en/rest_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activation_id` | path | `string` | yes | Activation run ID. |
