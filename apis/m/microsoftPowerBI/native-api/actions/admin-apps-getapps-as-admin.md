# Apps GetAppsAsAdmin with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `admin/apps`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Apps GetAppsAsAdmin](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/apps-get-apps-as-admin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | yes | The requested number of apps. |
| `$skip` | query | `number` | no | The number entries to be skipped. |
