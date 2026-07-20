# List Environments with Cloud CLI

Retrieves environments from Cloud CLI.

## Endpoint

- **Method:** `GET`
- **Path:** `/environments`
- **Base URL:** `https://cloudcli.ai/api/v1`
- **Official documentation:** [List Environments](https://developer.cloudcli.ai/list-environments-3998767e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Optional environment status to match. Accepted values: `0`, `1`, `2`, `3`, `4`. |
