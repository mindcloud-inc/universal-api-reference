# Delete Record with Stacker

Deletes a record from a Stacker object.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/external/objects/:object_sid/records/:record_sid/`
- **Base URL:** `https://api.go.stackerhq.com`
- **Official documentation:** [Delete Record](https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview/record-actions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `object_sid` | path | `string` | yes | Object SID from the Stacker endpoint path. |
| `record_sid` | path | `string` | yes | Record SID from the Stacker endpoint path. |
| `X-Account-Id` | body | `string` | yes | Stacker account ID sent as the X-Account-Id header. |
| `X-Stack-Id` | body | `string` | yes | Stacker stack ID sent as the X-Stack-Id header. |
