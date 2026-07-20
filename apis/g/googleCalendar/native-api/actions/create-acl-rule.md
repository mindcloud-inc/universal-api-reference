# Create ACL Rule with Google Calendar

Creates a new calendar ACL rule in Google Calendar.

## Endpoint

- **Method:** `POST`
- **Path:** `calendars/:calendar/acl`
- **Base URL:** `https://www.googleapis.com/calendar/v3`
- **Official documentation:** [Create ACL Rule](https://developers.google.com/workspace/calendar/api/v3/reference/acl/insert)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `calendar` | path | `list` | no |
| `role` | body | `string` | no |
| `scope.type` | body | `string` | no |
| `scope.value` | body | `string` | no |
