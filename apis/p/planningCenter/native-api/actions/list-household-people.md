# List Household People with Planning Center

Retrieves people in a household from Planning Center.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/v2/households/:household_id/people`
- **Base URL:** `https://api.planningcenteronline.com`
- **Official documentation:** [List Household People](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/household)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `household_id` | path | `string` | yes | The household id. |
| `non_pending` | query | `string` | no | Filter household people by non_pending. |
| `without_deceased` | query | `string` | no | Filter household people by without_deceased. |
