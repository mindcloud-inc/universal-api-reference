# TagManager create Container Version with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [TagManager create Container Version](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `idContainer` | body | `string` | yes | Matomo API parameter. |
| `name` | body | `string` | yes | Matomo API parameter. |
| `description` | body | `string` | no | Matomo API parameter. |
| `idContainerVersion` | body | `string` | no | Matomo API parameter. |
