# InformationProtection RemoveLabelsAsAdmin with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `admin/informationprotection/removeLabels`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [InformationProtection RemoveLabelsAsAdmin](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/information-protection-remove-labels-as-admin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dashboards[]` | body | `array<object>` | no | A list of unique dashboard IDs |
| `dataflows[]` | body | `array<object>` | no | A list of unique dataflow IDs |
| `datasets[]` | body | `array<string>` | no | A list of unique dataset IDs |
| `reports[]` | body | `array<object>` | no | A list of unique report IDs |
