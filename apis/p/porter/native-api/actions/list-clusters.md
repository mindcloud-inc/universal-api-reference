# List Clusters with Porter

Retrieves clusters from a Porter project.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/projects/:projectId/clusters`
- **Base URL:** `https://dashboard.porter.run`
- **Official documentation:** [List Clusters](https://docs.porter.run/standard/cli/command-reference/porter-cluster)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The Porter project ID whose clusters you want to list. |
