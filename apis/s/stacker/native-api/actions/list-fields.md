# List Fields with Stacker

Retrieves fields for a Stacker object.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/external/objects/:object_sid/fields/`
- **Base URL:** `https://api.go.stackerhq.com`
- **Official documentation:** [List Fields](https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview/accounts-stacks-objects-fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `object_sid` | path | `string` | yes | Object SID from the Stacker endpoint path. |
| `X-Account-Id` | body | `string` | yes | Stacker account ID sent as the X-Account-Id header. |
| `X-Stack-Id` | body | `string` | yes | Stacker stack ID sent as the X-Stack-Id header. |
