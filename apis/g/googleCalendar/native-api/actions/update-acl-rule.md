# Update ACL Rule with Google Calendar

Updates an existing calendar ACL rule in Google Calendar.

## Endpoint

- **Method:** `PATCH`
- **Path:** `calendars/:calendar/acl/:ruleId`
- **Base URL:** `https://www.googleapis.com/calendar/v3`
- **Official documentation:** [Update ACL Rule](https://developers.google.com/workspace/calendar/api/v3/reference/acl/patch)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `calendar` | path | `list` | no |
| `ruleId` | path | `string` | no |
| `role` | body | `string` | no |
