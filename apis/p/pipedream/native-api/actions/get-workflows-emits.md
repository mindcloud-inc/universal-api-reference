# Get workflow emits with Pipedream

Retrieves emitted event summaries for a workflow in Pipedream.

## Endpoint

- **Method:** `GET`
- **Path:** `/workflows/{workflow_id}/event_summaries`
- **Base URL:** `https://api.pipedream.com/v1`
- **Official documentation:** [Get workflow emits](https://pipedream.com/docs/rest-api/api-reference/workflows/get-workflows-emits)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_id` | path | `string` | yes | The workflow identifier. |
