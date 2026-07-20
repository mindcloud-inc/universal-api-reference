# TagManager add Container with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [TagManager add Container](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `context` | body | `string` | yes | Matomo API parameter. |
| `name` | body | `string` | yes | Matomo API parameter. |
| `description` | body | `string` | no | Matomo API parameter. |
| `ignoreGtmDataLayer` | body | `string` | no | Matomo API parameter. |
| `isTagFireLimitAllowedInPreviewMode` | body | `boolean` | no | Matomo API parameter. |
| `activelySyncGtmDataLayer` | body | `string` | no | Matomo API parameter. |
