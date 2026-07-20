# Register Webhook with Poodll

Registers a webhook for an event in Poodll.

## Endpoint

- **Method:** `POST`
- **Path:** `{baseUrl}/webservice/rest/server.php`
- **Base URL:** `{baseUrl}/webservice/rest/server.php`
- **Official documentation:** [Register Webhook](https://github.com/justinhunt/moodle-local_trigger/blob/master/externallib.php)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `event` | body | `string` | no |
| `hook` | body | `string` | no |
| `description` | body | `string` | no |
