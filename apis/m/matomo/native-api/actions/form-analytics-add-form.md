# FormAnalytics add Form with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [FormAnalytics add Form](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `name` | body | `string` | yes | Matomo API parameter. |
| `description` | body | `string` | no | Matomo API parameter. |
| `matchFormRules` | body | `string` | no | Matomo API parameter. |
| `matchPageRules` | body | `string` | no | Matomo API parameter. |
| `conversionRuleOption` | body | `string` | no | Matomo API parameter. |
| `conversionRules` | body | `string` | no | Matomo API parameter. |
| `idGoal` | body | `number` | no | Matomo API parameter. |
