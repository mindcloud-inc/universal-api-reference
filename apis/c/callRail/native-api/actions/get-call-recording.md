# Get Call Recording with CallRail

Retrieves a call recording from CallRail.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/a/:account_id/calls/:call_id/recording.json`
- **Base URL:** `https://api.callrail.com`
- **Official documentation:** [Get Call Recording](https://apidocs.callrail.com/#retrieving-a-single-call-recording)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `string` | yes | The CallRail account ID. |
| `call_id` | path | `string` | yes | The CallRail call ID. |
