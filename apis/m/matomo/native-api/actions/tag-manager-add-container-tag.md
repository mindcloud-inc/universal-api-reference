# TagManager add Container Tag with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [TagManager add Container Tag](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `idContainer` | body | `string` | yes | Matomo API parameter. |
| `idContainerVersion` | body | `string` | yes | Matomo API parameter. |
| `type` | body | `string` | yes | Matomo API parameter. |
| `name` | body | `string` | yes | Matomo API parameter. |
| `parameters` | body | `string` | no | Matomo API parameter. |
| `fireTriggerIds` | body | `string` | no | Matomo API parameter. |
| `blockTriggerIds` | body | `string` | no | Matomo API parameter. |
| `fireLimit` | body | `string` | no | Matomo API parameter. |
| `fireDelay` | body | `string` | no | Matomo API parameter. |
| `priority` | body | `string` | no | Matomo API parameter. |
| `startDate` | body | `string` | no | Matomo API parameter. |
| `endDate` | body | `string` | no | Matomo API parameter. |
| `description` | body | `string` | no | Matomo API parameter. |
| `status` | body | `string` | no | Matomo API parameter. |
