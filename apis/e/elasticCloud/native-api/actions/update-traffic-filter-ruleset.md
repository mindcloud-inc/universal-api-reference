# Update Traffic Filter Ruleset with Elastic Cloud

Updates an existing traffic filter ruleset in Elastic Cloud.

## Endpoint

- **Method:** `PUT`
- **Path:** `/deployments/traffic-filter/rulesets/:ruleset_id`
- **Base URL:** `https://api.elastic-cloud.com/api/v1`
- **Official documentation:** [Update Traffic Filter Ruleset](https://www.elastic.co/docs/api/doc/cloud/operation/operation-update-traffic-filter-ruleset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | The specification for the traffic filter ruleset. |
| `ruleset_id` | path | `string` | yes | Identifier for the ruleset. |
