# List Objects with Stacker

Retrieves objects from Stacker.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/external/objects/`
- **Base URL:** `https://api.go.stackerhq.com`
- **Official documentation:** [List Objects](https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview/accounts-stacks-objects-fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `X-Account-Id` | body | `string` | yes | Stacker account ID sent as the X-Account-Id header. |
| `X-Stack-Id` | body | `string` | yes | Stacker stack ID sent as the X-Stack-Id header. |
