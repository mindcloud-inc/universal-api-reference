# Unenrol Users with Poodll

Unenrols users from a Poodll course.

## Endpoint

- **Method:** `POST`
- **Path:** `{baseUrl}/webservice/rest/server.php`
- **Base URL:** `{baseUrl}/webservice/rest/server.php`
- **Official documentation:** [Unenrol Users](https://github.com/moodle/moodle/blob/MOODLE_405_STABLE/enrol/manual/externallib.php)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `enrolments[]` | body | `array<object>` | yes |
