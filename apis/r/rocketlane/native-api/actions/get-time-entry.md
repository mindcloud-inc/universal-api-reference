# Get Time Entry with Rocketlane

Retrieves a time entry from Rocketlane.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.0/time-entries/:timeEntryId`
- **Base URL:** `https://api.rocketlane.com/api`
- **Official documentation:** [Get Time Entry](https://developer.rocketlane.com/reference/get-time-entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `timeEntryId` | path | `number` | yes | The unique, system-generated identifier, which can be used to identify the time entry globally. |
| `includeFields` | query | `list<string>` | no | This query parameter allows you to specify which fields should be returned in the response body by selecting from the drop down. To get the relevant fields, use comma separated values. If the field is left blank, the default properties are returned. |
| `includeAllFields` | query | `boolean` | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |
