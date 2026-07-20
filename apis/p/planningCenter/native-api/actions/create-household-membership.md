# Create Household Membership with Planning Center

Creates a household membership in Planning Center.

## Endpoint

- **Method:** `POST`
- **Path:** `/people/v2/households/:household_id/household_memberships`
- **Base URL:** `https://api.planningcenteronline.com`
- **Official documentation:** [Create Household Membership](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/household_membership)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `household_id` | path | `string` | yes | The household id. |
| `data` | body | `object` | yes | JSON:API data object for the request payload. |
| `include` | query | `string` | no | Include the associated household or person in the response. |
