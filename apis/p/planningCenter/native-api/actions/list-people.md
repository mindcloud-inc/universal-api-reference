# List People with Planning Center

Retrieves people from Planning Center.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/v2/people`
- **Base URL:** `https://api.planningcenteronline.com`
- **Official documentation:** [List People](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/person)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include` | query | `string` | no | Include associated resources in the response. |
| `order` | query | `string` | no | Sort the returned people; prefix the field with a hyphen for descending order. |
| `filter` | query | `string` | no | — |
| `where[accounting_administrator]` | query | `boolean` | no | — |
| `where[anniversary]` | query | `date` | no | — |
| `where[birthdate]` | query | `date` | no | — |
| `where[child]` | query | `boolean` | no | — |
| `where[created_at]` | query | `date` | no | — |
| `where[first_name]` | query | `string` | no | — |
| `where[gender]` | query | `string` | no | — |
| `where[given_name]` | query | `string` | no | — |
| `where[grade]` | query | `number` | no | — |
| `where[graduation_year]` | query | `number` | no | — |
| `where[id]` | query | `string` | no | — |
| `where[inactivated_at]` | query | `date` | no | — |
| `where[last_name]` | query | `string` | no | — |
| `where[medical_notes]` | query | `string` | no | — |
| `where[membership]` | query | `string` | no | — |
| `where[mfa_configured]` | query | `boolean` | no | — |
| `where[middle_name]` | query | `string` | no | — |
| `where[nickname]` | query | `string` | no | — |
| `where[people_permissions]` | query | `string` | no | — |
| `where[primary_campus_id]` | query | `number` | no | — |
| `where[remote_id]` | query | `number` | no | — |
| `where[search_name]` | query | `string` | no | — |
| `where[search_name_or_email]` | query | `string` | no | — |
| `where[search_name_or_email_or_phone_number]` | query | `string` | no | — |
| `where[search_phone_number]` | query | `string` | no | — |
| `where[search_phone_number_e164]` | query | `string` | no | — |
| `where[site_administrator]` | query | `boolean` | no | — |
| `where[status]` | query | `string` | no | — |
| `where[updated_at]` | query | `date` | no | — |
