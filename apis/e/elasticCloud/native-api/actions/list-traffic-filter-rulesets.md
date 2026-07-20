# List Traffic Filter Rulesets with Elastic Cloud

Retrieves traffic filter rulesets from Elastic Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/deployments/traffic-filter/rulesets`
- **Base URL:** `https://api.elastic-cloud.com/api/v1`
- **Official documentation:** [List Traffic Filter Rulesets](https://www.elastic.co/docs/api/doc/cloud/operation/operation-get-traffic-filter-rulesets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_associations` | query | `boolean` | no | Include resources associated with each ruleset. |
| `organization_id` | query | `string` | no | Limit rulesets to the specified organization ID. Only takes effect for admins. |
| `region` | query | `string` | no | Limit rulesets to the specified region. |
