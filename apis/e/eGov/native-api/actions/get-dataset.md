# Get Dataset with e-Gov

Retrieves a dataset and its resources from e-Gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/package_show`
- **Base URL:** `https://data.e-gov.go.jp/data/api/action`
- **Official documentation:** [Get Dataset](https://data.e-gov.go.jp/data/api/3/action/help_show?name=package_show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Dataset identifier or dataset name. |
