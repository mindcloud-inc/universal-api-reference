# Get Traffic Filter Ruleset with Elastic Cloud

Retrieves a traffic filter ruleset from Elastic Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/deployments/traffic-filter/rulesets/:ruleset_id`
- **Base URL:** `https://api.elastic-cloud.com/api/v1`
- **Official documentation:** [Get Traffic Filter Ruleset](https://www.elastic.co/docs/api/doc/cloud/operation/operation-get-traffic-filter-ruleset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_associations` | query | `boolean` | no | Include resources associated with the ruleset. |
| `ruleset_id` | path | `string` | yes | Identifier for the ruleset. |
