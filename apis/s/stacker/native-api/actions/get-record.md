# Get Record with Stacker

Retrieves a record from a Stacker object.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/external/objects/:object_sid/records/:record_sid/`
- **Base URL:** `https://api.go.stackerhq.com`
- **Official documentation:** [Get Record](https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview/record-actions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_fields` | query | `string` | no | JSON array string of field API names to include in the response. |
| `object_sid` | path | `string` | yes | Object SID from the Stacker endpoint path. |
| `record_sid` | path | `string` | yes | Record SID from the Stacker endpoint path. |
| `X-Account-Id` | body | `string` | yes | Stacker account ID sent as the X-Account-Id header. |
| `X-Stack-Id` | body | `string` | yes | Stacker stack ID sent as the X-Stack-Id header. |
