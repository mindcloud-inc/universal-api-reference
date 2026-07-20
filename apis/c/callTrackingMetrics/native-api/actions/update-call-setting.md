# Update Call Setting with CallTrackingMetrics

Updates an existing call setting in CallTrackingMetrics.

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts/:accountId/call_settings/:callSettingId.json`
- **Base URL:** `https://api.calltrackingmetrics.com/api/v1`
- **Official documentation:** [Update Call Setting](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/ebpj2uv/update-call-setting)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `callSettingId` | path | `string` | yes | The CallTrackingMetrics call setting ID. |
| `description` | body | `string` | no | An updated description for the call setting. |
