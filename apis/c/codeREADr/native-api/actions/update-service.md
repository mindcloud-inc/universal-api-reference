# Update Service with CodeREADr

Updates an existing scanning service in CodeREADr.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/`
- **Base URL:** `https://api.codereadr.com`
- **Official documentation:** [Update Service](https://secure.codereadr.com/apidocs/Services.md#edit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `service_id` | body | `string` | yes | Service to update. |
| `validation_method` | body | `string` | no | Optional new validation method. |
| `database_id` | body | `string` | no | Used with database or ondevicedatabase services. |
| `postback_url` | body | `string` | no | Used with postback services or postback settings. |
| `service_name` | body | `string` | no | Optional new service name. |
| `description` | body | `string` | no | Optional description or webview content update. |
