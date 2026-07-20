# MultiChannelConversionAttribution get Channel Attribution with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [MultiChannelConversionAttribution get Channel Attribution](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `period` | body | `string` | yes | Matomo API parameter. |
| `date` | body | `string` | yes | Matomo API parameter. |
| `idGoal` | body | `number` | yes | Matomo API parameter. |
| `idCampaignDimensionCombination` | body | `string` | no | Matomo API parameter. |
| `segment` | body | `string` | no | Matomo API parameter. |
| `expanded` | body | `boolean` | no | Matomo API parameter. |
| `flat` | body | `boolean` | no | Matomo API parameter. |
| `idSubtable` | body | `number` | no | Matomo API parameter. |
