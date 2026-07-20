# Update Benefit Category with TalentHR

Updates an existing benefit category in TalentHR.

## Endpoint

- **Method:** `PUT`
- **Path:** `/benefit-categories/:objectId`
- **Base URL:** `https://pubapi.talenthr.io/v1`
- **Official documentation:** [Update Benefit Category](https://apidocs.talenthr.io/#88073194-9944-40fd-839c-0a45f5609e0b)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `objectId` | path | `number` | yes | TalentHR benefit category ID. |
| `name` | body | `string` | yes | Benefit category name. |
