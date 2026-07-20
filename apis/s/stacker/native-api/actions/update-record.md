# Update Record with Stacker

Updates an existing record in a Stacker object.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/external/objects/:object_sid/records/:record_sid/`
- **Base URL:** `https://api.go.stackerhq.com`
- **Official documentation:** [Update Record](https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview/record-actions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_fields[]` | body | `array<string>` | no | Field API names to include in the update response. |
| `object_sid` | path | `string` | yes | Object SID from the Stacker endpoint path. |
| `record_sid` | path | `string` | yes | Record SID from the Stacker endpoint path. |
| `X-Account-Id` | body | `string` | yes | Stacker account ID sent as the X-Account-Id header. |
| `X-Stack-Id` | body | `string` | yes | Stacker stack ID sent as the X-Stack-Id header. |
