# List Person Addresses with Planning Center

Retrieves addresses for a person in Planning Center.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/v2/people/:person_id/addresses`
- **Base URL:** `https://api.planningcenteronline.com`
- **Official documentation:** [List Person Addresses](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/address)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `person_id` | path | `string` | yes |
| `order` | query | `string` | no |
| `where[city]` | query | `string` | no |
| `where[country_code]` | query | `string` | no |
| `where[location]` | query | `string` | no |
| `where[primary]` | query | `boolean` | no |
| `where[state]` | query | `string` | no |
| `where[street_line_1]` | query | `string` | no |
| `where[street_line_2]` | query | `string` | no |
| `where[zip]` | query | `string` | no |
