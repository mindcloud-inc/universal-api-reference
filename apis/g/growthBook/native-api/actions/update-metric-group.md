# Update a single metricGroup with GrowthBook

Updates an existing metric group in GrowthBook.

## Endpoint

- **Method:** `PUT`
- **Path:** `/metric-groups/:id`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Update a single metricGroup](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `name` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `tags` | body | `list<string>` | no | — |
| `projects` | body | `list<string>` | no | — |
| `metrics` | body | `list<string>` | no | — |
| `datasource` | body | `string` | no | — |
| `owner` | body | `string` | no | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `archived` | body | `boolean` | no | — |
