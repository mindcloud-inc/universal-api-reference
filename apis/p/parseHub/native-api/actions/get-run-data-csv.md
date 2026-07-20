# Get Run Data (CSV) with ParseHub

## Endpoint

- **Method:** `GET`
- **Path:** `/runs/{run_token}/data`
- **Base URL:** `https://www.parsehub.com/api/v2`
- **Official documentation:** [Get Run Data (CSV)](https://www.parsehub.com/docs/ref/api/v2/#get-data-for-a-run)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_token` | path | `string` | yes | The ParseHub token of the run whose extracted CSV you want. |
