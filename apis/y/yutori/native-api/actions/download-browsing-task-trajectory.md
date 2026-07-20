# Download Browsing Task Trajectory with Yutori

Downloads the trajectory of a completed Yutori browsing task.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/browsing/tasks/:id/trajectory`
- **Base URL:** `https://api.yutori.com`
- **Official documentation:** [Download Browsing Task Trajectory](https://docs.yutori.com/reference/browsing-trajectory)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `output_type` | query | `string` | no |
