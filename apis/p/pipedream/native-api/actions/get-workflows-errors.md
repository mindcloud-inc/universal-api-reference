# Get workflow errors with Pipedream

Retrieves error event summaries for a workflow in Pipedream.

## Endpoint

- **Method:** `GET`
- **Path:** `/workflows/{workflow_id}/$errors/event_summaries`
- **Base URL:** `https://api.pipedream.com/v1`
- **Official documentation:** [Get workflow errors](https://pipedream.com/docs/rest-api/api-reference/workflows/get-workflows-errors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_id` | path | `string` | yes | The workflow identifier. |
