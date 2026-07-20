# Transitions get Transitions For Action with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [Transitions get Transitions For Action](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actionName` | body | `string` | yes | Matomo API parameter. |
| `actionType` | body | `string` | yes | Matomo API parameter. |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `period` | body | `string` | yes | Matomo API parameter. |
| `date` | body | `string` | yes | Matomo API parameter. |
| `segment` | body | `string` | no | Matomo API parameter. |
| `limitBeforeGrouping` | body | `string` | no | Matomo API parameter. |
| `parts` | body | `string` | no | Matomo API parameter. |
