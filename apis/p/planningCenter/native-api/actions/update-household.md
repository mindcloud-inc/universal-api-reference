# Update Household with Planning Center

Updates an existing household in Planning Center.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/people/v2/households/:id`
- **Base URL:** `https://api.planningcenteronline.com`
- **Official documentation:** [Update Household](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/household)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The household id. |
| `data` | body | `object` | yes | JSON:API data object for the request payload. |
| `include` | query | `string` | no | Include associated people in the response. |
