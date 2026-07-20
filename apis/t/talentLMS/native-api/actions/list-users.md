# List Users with TalentLMS

Retrieves users from a TalentLMS domain.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://{domain}.talentlms.com/api/v2`
- **Official documentation:** [List Users](https://documenter.getpostman.com/view/31867199/2sAY548Kou#list-all-users)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page[number]` | query | `number` | no | Page number for paginated results (starts at 1). |
| `page[size]` | query | `number` | no | Number of records per page (max 100). |
| `filter[login][eq]` | query | `string` | no | Filter users by exact login. |
| `filter[email][eq]` | query | `string` | no | Filter users by exact email. |
| `filter[custom_field_value][eq]` | query | `string` | no | Filter users by custom field value. |
