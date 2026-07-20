# SitesManager get Image Tracking Code with Matomo

## Endpoint

- **Method:** `POST`
- **Path:** `/index.php`
- **Base URL:** `https://mindcloud.matomo.cloud`
- **Official documentation:** [SitesManager get Image Tracking Code](https://developer.matomo.org/api-reference/reporting-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idSite` | body | `number` | yes | Matomo API parameter. |
| `piwikUrl` | body | `string` | no | Matomo API parameter. |
| `actionName` | body | `string` | no | Matomo API parameter. |
| `idGoal` | body | `number` | no | Matomo API parameter. |
| `revenue` | body | `string` | no | Matomo API parameter. |
| `forceMatomoEndpoint` | body | `boolean` | no | Matomo API parameter. |
