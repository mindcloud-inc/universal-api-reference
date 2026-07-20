# Update Department with TalentLyft

Updates an existing department in TalentLyft.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/departments/:id`
- **Base URL:** `https://api.talentlyft.com`
- **Official documentation:** [Update Department](https://developers.talentlyft.com/customer-api-reference/departments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The TalentLyft department ID. |
| `Name` | body | `string` | no | The new department name. |
| `ExternalId` | body | `string` | no | Optional external identifier for the department. |
| `ParentId` | body | `number` | no | Optional parent department ID. |
