# Get Folder By UID with Grafana

Retrieves a folder from Grafana by UID.

## Endpoint

- **Method:** `GET`
- **Path:** `/folders/:folder_uid`
- **Base URL:** `https://apps78aa.grafana.net/api`
- **Official documentation:** [Get Folder By UID](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/folder/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_uid` | path | `string` | yes | The folder UID. |
