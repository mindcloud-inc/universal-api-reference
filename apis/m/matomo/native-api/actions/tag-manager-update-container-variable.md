# TagManager update Container Variable with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [TagManager update Container Variable](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `idContainer` | body | `string` | yes | Matomo API parameter. |
| `idContainerVersion` | body | `string` | yes | Matomo API parameter. |
| `idVariable` | body | `string` | yes | Matomo API parameter. |
| `name` | body | `string` | yes | Matomo API parameter. |
| `parameters` | body | `string` | no | Matomo API parameter. |
| `defaultValue` | body | `string` | no | Matomo API parameter. |
| `lookupTable` | body | `string` | no | Matomo API parameter. |
| `description` | body | `string` | no | Matomo API parameter. |
