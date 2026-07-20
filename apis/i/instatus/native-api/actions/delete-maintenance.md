# Delete Maintenance with Instatus

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/:page_id/maintenances/:maintenance_id`
- **Base URL:** `https://api.instatus.com`
- **Official documentation:** [Delete Maintenance](https://instatus.com/help/api/maintenances)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_id` | path | `string` | yes | Instatus status page ID. |
| `maintenance_id` | path | `string` | yes | Instatus maintenance ID. |
