# CustomDimensions configure New Custom Dimension with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [CustomDimensions configure New Custom Dimension](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `name` | body | `string` | yes | Matomo API parameter. |
| `scope` | body | `string` | yes | Matomo API parameter. |
| `active` | body | `string` | yes | Matomo API parameter. |
| `extractions` | body | `string` | no | Matomo API parameter. |
| `caseSensitive` | body | `string` | no | Matomo API parameter. |
