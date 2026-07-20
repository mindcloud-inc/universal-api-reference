# Create a single metricGroup with GrowthBook

Creates a new metric group in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/metric-groups`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create a single metricGroup](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `description` | body | `string` | yes | — |
| `tags` | body | `list<string>` | no | — |
| `projects` | body | `list<string>` | yes | — |
| `metrics` | body | `list<string>` | yes | — |
| `datasource` | body | `string` | yes | — |
| `owner` | body | `string` | no | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `archived` | body | `boolean` | no | — |
