# List Course Members with TrainerCentral

Retrieves course members from TrainerCentral.

## Endpoint

- **Method:** `GET`
- **Path:** `/course/:courseId/courseMembers.json`
- **Base URL:** `{academyUrl}/api/v4/{orgId}`
- **Official documentation:** [List Course Members](https://help.trainercentral.com/portal/en/kb/articles/how-do-i-get-coursememberid)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `courseId` | path | `string` | yes | The TrainerCentral course ID whose learner membership list should be fetched. |
| `searchText` | query | `string` | no | Optional learner name search text. |
