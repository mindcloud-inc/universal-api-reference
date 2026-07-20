# Run Stage0 Activity with Inistate

Performs a Stage0 activity on an entry in Inistate.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/activity`
- **Base URL:** `https://api.inistate.com`
- **Official documentation:** [Run Stage0 Activity](https://app.swaggerhub.com/apis-docs/Inistate/InistateAPI/1.0.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activityId` | body | `string` | yes | Provider activity ID such as `Create` or `Edit`. |
| `entryId` | body | `number` | no | Existing entry ID for edit or other entry-scoped activities. |
| `payload` | body | `object` | no | Optional field payload keyed by provider field names. |
