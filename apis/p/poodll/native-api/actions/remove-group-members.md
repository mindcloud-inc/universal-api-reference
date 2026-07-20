# Remove Group Members with Poodll

Removes members from a group in Poodll.

## Endpoint

- **Method:** `POST`
- **Path:** `{baseUrl}/webservice/rest/server.php`
- **Base URL:** `{baseUrl}/webservice/rest/server.php`
- **Official documentation:** [Remove Group Members](https://github.com/moodle/moodle/blob/MOODLE_405_STABLE/group/externallib.php)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `members[]` | body | `array<object>` | yes |
