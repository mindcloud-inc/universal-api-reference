# Get Directory with TalentHR

Retrieves the employee directory from TalentHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/directory`
- **Base URL:** `https://pubapi.talenthr.io/v1`
- **Official documentation:** [Get Directory](https://apidocs.talenthr.io/#7d5408ba-aa8b-4187-bd0e-0e347cdea5d0)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of employees to return. TalentHR defaults to 10 when this is omitted. |
| `offset` | query | `number` | no | Pagination offset. Use -1 to disable pagination for this endpoint. |
| `filter` | query | `string` | no | Optional directory filter ID. Use the Directory Filters endpoint to discover valid filter IDs before using this field. |
