# Update Metrics Filter Template with Pitchbox

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/metric_filter_templates/:id`
- **Base URL:** `https://apiv2.pitchbox.com`
- **Official documentation:** [Update Metrics Filter Template](https://apiv2.pitchbox.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The metrics filter template id. |
| `name` | body | `string` | yes | The updated metrics filter template name. |
| `visibility` | body | `string` | no | The metrics filter template visibility. |
