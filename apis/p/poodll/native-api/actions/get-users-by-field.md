# Get Users By Field with Poodll

Finds users in Poodll by a specific field.

## Endpoint

- **Method:** `POST`
- **Path:** `{baseUrl}/webservice/rest/server.php`
- **Base URL:** `{baseUrl}/webservice/rest/server.php`
- **Official documentation:** [Get Users By Field](https://github.com/moodle/moodle/blob/MOODLE_405_STABLE/user/externallib.php)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `field` | body | `string` | yes |
| `values[]` | body | `array<string>` | yes |
