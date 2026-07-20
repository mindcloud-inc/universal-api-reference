# Update a metric with GrowthBook

Updates an existing metric in GrowthBook.

## Endpoint

- **Method:** `PUT`
- **Path:** `/metrics/:id`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Update a metric](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the requested resource |
| `managedBy` | body | `string` | no | Where this metric must be managed from. If not set (empty string), it can be managed from anywhere. If set to "api", it can be managed via the API only. Please note that we have deprecated support for setting the managedBy property to "admin". Your existing Legacy Metrics with this value will continue to work, but we suggest migrating to Fact Metrics instead. |
| `owner` | body | `string` | no | The userId or email address of the owner. If an email address is provided, it will be used to look up the userId of the matching organization member. If an ID is provided, it will be validated as existing in the organization. |
| `name` | body | `string` | no | Name of the metric |
| `description` | body | `string` | no | Description of the metric |
| `type` | body | `string` | no | Type of metric. See [Metrics documentation](/app/metrics/legacy) |
| `tags` | body | `list<string>` | no | List of tags |
| `projects` | body | `list<string>` | no | List of project IDs for projects that can access this metric |
| `archived` | body | `boolean` | no | — |
| `behavior` | body | `object` | no | — |
| `sql` | body | `object` | no | Preferred way to define SQL. Only one of `sql`, `sqlBuilder` or `mixpanel` allowed. |
| `sqlBuilder` | body | `object` | no | An alternative way to specify a SQL metric, rather than a full query. Using `sql` is preferred to `sqlBuilder`. Only one of `sql`, `sqlBuilder` or `mixpanel` allowed |
| `mixpanel` | body | `object` | no | Only use for MixPanel (non-SQL) Data Sources. Only one of `sql`, `sqlBuilder` or `mixpanel` allowed. |
