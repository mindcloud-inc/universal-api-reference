# Delete Protection Plan with Acronis

Deletes an existing protection plan from Acronis.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/policy_management/v4/policies/{policy_id}`
- **Base URL:** `{dataCenterUrl}`
- **Official documentation:** [Delete Protection Plan](https://developer.acronis.com/doc/outbound/apis/api-library/resource-policy/policies/deleting-plan.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policy_id` | path | `string` | yes | Policy Id path parameter. |
