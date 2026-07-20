# Get Folder Descendant Counts with Grafana

Retrieves descendant counts for a folder in Grafana.

## Endpoint

- **Method:** `GET`
- **Path:** `/folders/:folder_uid/counts`
- **Base URL:** `https://apps78aa.grafana.net/api`
- **Official documentation:** [Get Folder Descendant Counts](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/folder/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_uid` | path | `string` | yes | The folder UID. |
