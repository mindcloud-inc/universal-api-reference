# List Stacks with Stacker

Retrieves stacks from Stacker.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/external/stacks/`
- **Base URL:** `https://api.go.stackerhq.com`
- **Official documentation:** [List Stacks](https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview/accounts-stacks-objects-fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `X-Account-Id` | body | `string` | yes | Stacker account ID sent as the X-Account-Id header. |
