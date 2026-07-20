# Update Division with TalentHR

Updates an existing division in TalentHR.

## Endpoint

- **Method:** `PUT`
- **Path:** `/divisions/:objectId`
- **Base URL:** `https://pubapi.talenthr.io/v1`
- **Official documentation:** [Update Division](https://apidocs.talenthr.io/#aff24708-0102-4f32-b8f5-deccff71235b)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `objectId` | path | `number` | yes | Division ID. |
| `name` | body | `string` | yes | Division name. |
