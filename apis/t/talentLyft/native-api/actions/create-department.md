# Create Department with TalentLyft

Creates a new department in TalentLyft.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/departments`
- **Base URL:** `https://api.talentlyft.com`
- **Official documentation:** [Create Department](https://developers.talentlyft.com/customer-api-reference/departments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | The department name. |
| `ExternalId` | body | `string` | no | Optional external identifier for the department. |
| `ParentId` | body | `number` | no | Optional parent department ID. |
