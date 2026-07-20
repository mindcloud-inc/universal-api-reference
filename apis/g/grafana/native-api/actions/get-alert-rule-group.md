# Get Alert Rule Group with Grafana

Retrieves an alert rule group from Grafana.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/provisioning/folder/:FolderUID/rule-groups/:Group`
- **Base URL:** `https://apps78aa.grafana.net/api`
- **Official documentation:** [Get Alert Rule Group](https://grafana.com/docs/grafana/latest/alerting/set-up/provision-alerting-resources/http-api-provisioning/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FolderUID` | path | `string` | yes | The folder UID. |
| `Group` | path | `string` | yes | The alert rule group name. |
