# Get Folder Permissions with Grafana

Retrieves folder permissions from Grafana.

## Endpoint

- **Method:** `GET`
- **Path:** `/folders/:folder_uid/permissions`
- **Base URL:** `https://apps78aa.grafana.net/api`
- **Official documentation:** [Get Folder Permissions](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/folder_permissions/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_uid` | path | `string` | yes | The folder UID. |
