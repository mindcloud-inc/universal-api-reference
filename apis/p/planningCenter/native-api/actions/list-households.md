# List Households with Planning Center

Retrieves households from Planning Center.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/v2/households`
- **Base URL:** `https://api.planningcenteronline.com`
- **Official documentation:** [List Households](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/household)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include` | query | `string` | no | Include associated people in the response. |
| `order` | query | `string` | no | Sort households by a supported field; prefix the field with a hyphen for descending order. |
| `where` | query | `object` | no | Field-qualified household query filters. |
| `where[created_at]` | query | `date` | no | Query households by an exact created_at timestamp in ISO 8601 format. |
| `where[member_count]` | query | `number` | no | Query households by an exact member_count value. |
| `where[name]` | query | `string` | no | Query households by an exact household name. |
| `where[primary_contact_name]` | query | `string` | no | Query households by an exact primary_contact_name value. |
| `where[updated_at]` | query | `date` | no | Query households by an exact updated_at timestamp in ISO 8601 format. |
