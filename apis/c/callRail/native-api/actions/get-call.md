# Get Call with CallRail

Retrieves a call from CallRail.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/a/:account_id/calls/:call_id.json`
- **Base URL:** `https://api.callrail.com`
- **Official documentation:** [Get Call](https://apidocs.callrail.com/#retrieving-a-single-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `string` | yes | The CallRail account ID. |
| `call_id` | path | `string` | yes | The CallRail call ID. |
| `fields` | query | `string` | no | Optional comma-separated additional call fields to return. |
