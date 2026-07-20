# List Group Members with ActiveTrail

Retrieves members of a group from ActiveTrail.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:id/members`
- **Base URL:** `https://webapi.mymarketing.co.il/api`
- **Official documentation:** [List Group Members](https://webapi.mymarketing.co.il/api/docs/and/Api/GET-api-groups-id-members_CustomerStates_SearchTerm_FromDate_ToDate_Page_Limit)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_states` | query | `list<string>` | yes | Choose the states of the contacts you want to get. Accepted values: `ACTIVE`, `ALL`, `BOUNCED`, `CUSTOMER_REQUEST`, `INACTIVE`, `QUARANTINED`, `SPAM_COMPLIENT`. |
| `from_date` | query | `date` | no | Only include members from this date forward. |
| `id` | path | `number` | yes | Group id. Can be found using the account groups endpoint or in the UI. |
| `search_term` | query | `string` | no | Search group members by a free-text term. |
| `to_date` | query | `date` | no | Only include members up to this date. |
