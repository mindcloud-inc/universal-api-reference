# Goals add Goal with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [Goals add Goal](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `name` | body | `string` | yes | Matomo API parameter. |
| `matchAttribute` | body | `string` | yes | Matomo API parameter. |
| `pattern` | body | `string` | yes | Matomo API parameter. |
| `patternType` | body | `string` | yes | Matomo API parameter. |
| `caseSensitive` | body | `string` | no | Matomo API parameter. |
| `revenue` | body | `string` | no | Matomo API parameter. |
| `allowMultipleConversionsPerVisit` | body | `string` | no | Matomo API parameter. |
| `description` | body | `string` | no | Matomo API parameter. |
| `useEventValueAsRevenue` | body | `string` | no | Matomo API parameter. |
