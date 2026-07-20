# Refresh Data Source with Griptape

Creates a data source refresh job in Griptape.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/data-connectors/:data_source_id/data-jobs`
- **Base URL:** `https://cloud.griptape.ai`
- **Official documentation:** [Refresh Data Source](https://docs.griptape.ai/stable/griptape-cloud/data-sources/refresh-data/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data_source_id` | path | `string` | yes | The data source ID to refresh. |
