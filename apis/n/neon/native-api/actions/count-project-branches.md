# Retrieve number of branches with Neon

Retrieves the number of branches from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/branches/count`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Retrieve number of branches](https://api-docs.neon.tech/reference/countprojectbranches)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | no | Neon API parameter project_id |
| `search` | query | `string` | no | Count branches matching the name in the search query |
