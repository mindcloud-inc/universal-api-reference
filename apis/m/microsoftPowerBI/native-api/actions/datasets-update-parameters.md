# Update Parameters with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `datasets/[:datasetId]/Default.UpdateParameters`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Update Parameters](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/update-parameters)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The dataset ID |
| `updateDetails[]` | body | `array<object>` | yes | A list of dataset parameters to update |
