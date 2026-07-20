# Delete Traffic Filter Ruleset with Elastic Cloud

Deletes an existing traffic filter ruleset from Elastic Cloud.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/deployments/traffic-filter/rulesets/:ruleset_id`
- **Base URL:** `https://api.elastic-cloud.com/api/v1`
- **Official documentation:** [Delete Traffic Filter Ruleset](https://www.elastic.co/docs/api/doc/cloud/operation/operation-delete-traffic-filter-ruleset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ignore_associations` | query | `boolean` | no | Delete the ruleset even when associations exist. |
| `ruleset_id` | path | `string` | yes | Identifier for the ruleset. |
