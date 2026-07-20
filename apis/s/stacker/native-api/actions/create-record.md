# Create Record with Stacker

Creates a new record in a Stacker object.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/external/objects/:object_sid/records/`
- **Base URL:** `https://api.go.stackerhq.com`
- **Official documentation:** [Create Record](https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview/record-actions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_fields[]` | body | `array<string>` | no | Field API names to include in the create response. |
| `object_sid` | path | `string` | yes | Object SID from the Stacker endpoint path. |
| `X-Account-Id` | body | `string` | yes | Stacker account ID sent as the X-Account-Id header. |
| `X-Stack-Id` | body | `string` | yes | Stacker stack ID sent as the X-Stack-Id header. |
