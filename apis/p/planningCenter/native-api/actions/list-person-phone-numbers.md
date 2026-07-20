# List Person Phone Numbers with Planning Center

Retrieves phone numbers for a person in Planning Center.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/v2/people/:person_id/phone_numbers`
- **Base URL:** `https://api.planningcenteronline.com`
- **Official documentation:** [List Person Phone Numbers](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/phone_number)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `person_id` | path | `string` | yes |
| `order` | query | `string` | no |
| `where[carrier]` | query | `string` | no |
| `where[created_at]` | query | `date` | no |
| `where[location]` | query | `string` | no |
| `where[number]` | query | `string` | no |
| `where[primary]` | query | `boolean` | no |
| `where[updated_at]` | query | `date` | no |
