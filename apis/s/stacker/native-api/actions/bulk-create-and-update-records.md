# Bulk Create and Update Records with Stacker

Creates or updates records in a Stacker object.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/external/objects/:object_sid/bulk-records/`
- **Base URL:** `https://api.go.stackerhq.com`
- **Official documentation:** [Bulk Create and Update Records](https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview/record-actions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `object_sid` | path | `string` | yes | Object SID from the Stacker endpoint path. |
| `records[]` | body | `array<object>` | yes | Array of record objects using Stacker field API names. Include `_sid` to update an existing record. |
| `X-Account-Id` | body | `string` | yes | Stacker account ID sent as the X-Account-Id header. |
| `X-Stack-Id` | body | `string` | yes | Stacker stack ID sent as the X-Stack-Id header. |
