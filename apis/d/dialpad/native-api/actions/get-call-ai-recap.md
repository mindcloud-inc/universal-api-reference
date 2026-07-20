# Get Call AI Recap with Dialpad

Retrieves an AI recap for a Dialpad call.

## Endpoint

- **Method:** `GET`
- **Path:** `/call/:id/ai_recap`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [Get Call AI Recap](https://developers.dialpad.com/reference/callai_recap)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The call's id. |
| `summary_format` | query | `string` | no | The format of the summary to retrieve. |
