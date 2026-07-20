# Update Statuspage Status with Pinghome

Updates statuspage status in Pinghome.

## Endpoint

- **Method:** `PUT`
- **Path:** `/statuspage-cmd/v1/statuspage/:id/status`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [Update Statuspage Status](https://docs.pinghome.io/statuspages/update-statuspage-status/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the statuspage. |
| `enabled` | body | `boolean` | yes | Whether the statuspage should be enabled. |
