# Get workspaces's sources with Pipedream

Retrieves sources for a workspace from Pipedream.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/{org_id}/sources`
- **Base URL:** `https://api.pipedream.com/v1`
- **Official documentation:** [Get workspaces's sources](https://pipedream.com/docs/rest-api/api-reference/workspaces/get-workspaces-sources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | The workspace identifier. |
