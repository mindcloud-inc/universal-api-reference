# Get workspaces's subscriptions with Pipedream

Retrieves subscriptions for a workspace from Pipedream.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/{org_id}/subscriptions`
- **Base URL:** `https://api.pipedream.com/v1`
- **Official documentation:** [Get workspaces's subscriptions](https://pipedream.com/docs/rest-api/api-reference/workspaces/get-workspaces-subscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | The workspace identifier. |
