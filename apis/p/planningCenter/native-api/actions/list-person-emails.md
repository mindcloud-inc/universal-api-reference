# List Person Emails with Planning Center

Retrieves email addresses for a person in Planning Center.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/v2/people/:person_id/emails`
- **Base URL:** `https://api.planningcenteronline.com`
- **Official documentation:** [List Person Emails](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/email)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `person_id` | path | `string` | yes |
| `order` | query | `string` | no |
| `where[address]` | query | `string` | no |
| `where[blocked]` | query | `boolean` | no |
| `where[created_at]` | query | `date` | no |
| `where[location]` | query | `string` | no |
| `where[primary]` | query | `boolean` | no |
| `where[updated_at]` | query | `date` | no |
