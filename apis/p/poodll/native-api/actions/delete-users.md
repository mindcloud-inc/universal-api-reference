# Delete Users with Poodll

Deletes existing user accounts from Poodll.

## Endpoint

- **Method:** `POST`
- **Path:** `{baseUrl}/webservice/rest/server.php`
- **Base URL:** `{baseUrl}/webservice/rest/server.php`
- **Official documentation:** [Delete Users](https://github.com/moodle/moodle/blob/MOODLE_405_STABLE/user/externallib.php)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `userids[]` | body | `array<number>` | yes |
