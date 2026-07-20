# Update Agency Integration with EasyBroker

Updates an agency integration status in EasyBroker.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/integration_partners/agencies/:agency_id/integration`
- **Base URL:** `https://api.easybroker.com/v1`
- **Official documentation:** [Update Agency Integration](https://dev.easybroker.com/reference/patch_agencies-agency-id-integration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agency_id` | path | `string` | yes | The EasyBroker agency ID. |
| `status` | body | `string` | yes | Accepted values: paused and connected. |
| `status_reason` | body | `string` | no | Required only when status is paused. |
