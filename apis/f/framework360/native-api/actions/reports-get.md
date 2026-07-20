# Get Report with Framework360

## Endpoint

- **Method:** `POST`
- **Path:** `reports/get`
- **Base URL:** `https://mindcloudstage0.framework360.site/m/api`
- **Official documentation:** [Get Report](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | body | `string` | yes | Report category. |
| `item` | body | `string` | yes | Specific report item. |
| `filters` | body | `object` | no | Report filters. |
| `sort[]` | body | `array<string>` | no | Sort configuration. |
| `type` | body | `string` | yes | Report output type. |
