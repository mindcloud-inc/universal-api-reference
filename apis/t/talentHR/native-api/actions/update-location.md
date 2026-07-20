# Update Location with TalentHR

Updates an existing location in TalentHR.

## Endpoint

- **Method:** `PUT`
- **Path:** `/locations/:objectId`
- **Base URL:** `https://pubapi.talenthr.io/v1`
- **Official documentation:** [Update Location](https://apidocs.talenthr.io/#c517de21-64eb-479f-bb71-82d9a198a045)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `objectId` | path | `number` | yes | Location ID. |
| `name` | body | `string` | yes | Location name. |
| `field_data` | body | `object` | yes | Location field data object with address and is_remote. |
