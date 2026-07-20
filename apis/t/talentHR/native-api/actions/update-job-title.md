# Update Job Title with TalentHR

Updates an existing job title in TalentHR.

## Endpoint

- **Method:** `PUT`
- **Path:** `/job-titles/:objectId`
- **Base URL:** `https://pubapi.talenthr.io/v1`
- **Official documentation:** [Update Job Title](https://apidocs.talenthr.io/#372cca97-bc1c-4b16-96b2-68837913b6d8)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `objectId` | path | `number` | yes | Job title ID. |
| `name` | body | `string` | yes | Job title name. |
