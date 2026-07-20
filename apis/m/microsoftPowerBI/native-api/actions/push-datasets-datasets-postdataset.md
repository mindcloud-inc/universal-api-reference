# Datasets PostDataset with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `datasets`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Datasets PostDataset](https://learn.microsoft.com/en-us/rest/api/power-bi/push-datasets/datasets-post-dataset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `defaultRetentionPolicy` | query | `object` | no | The default retention policy |
| `name` | body | `string` | yes | The dataset name |
| `tables[]` | body | `array<object>` | yes | The dataset tables |
| `datasources[]` | body | `array<object>` | no | The data sources associated with this dataset |
| `defaultMode` | body | `object` | no | The dataset mode or type |
| `relationships[]` | body | `array<object>` | no | The dataset relationships |
