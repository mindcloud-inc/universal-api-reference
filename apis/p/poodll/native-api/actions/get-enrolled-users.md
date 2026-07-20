# Get Enrolled Users with Poodll

Retrieves enrolled users from a Poodll course.

## Endpoint

- **Method:** `POST`
- **Path:** `{baseUrl}/webservice/rest/server.php`
- **Base URL:** `{baseUrl}/webservice/rest/server.php`
- **Official documentation:** [Get Enrolled Users](https://github.com/moodle/moodle/blob/MOODLE_405_STABLE/enrol/externallib.php)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `courseid` | body | `number` | yes |
| `options[]` | body | `array<object>` | no |
