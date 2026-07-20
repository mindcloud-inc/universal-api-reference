# Get Complete Organization Info with Apollo

Retrieves complete organization information from Apollo.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/organizations/:id`
- **Base URL:** `https://app.apollo.io/api`
- **Official documentation:** [Get Complete Organization Info](https://docs.apollo.io/reference/get-complete-organization-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Apollo ID for the organization that you want to research. To find organization IDs, call the Organization Search endpoint and identify the `organizaton_id` value for the organization. Example: `5e66b6381e05b4008c8331b8` |
