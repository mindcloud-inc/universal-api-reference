# Create Service with CodeREADr

Creates a new scanning service in CodeREADr.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/`
- **Base URL:** `https://api.codereadr.com`
- **Official documentation:** [Create Service](https://secure.codereadr.com/apidocs/Services.md#create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `validation_method` | body | `string` | yes | Service type to create, such as record, database, postback, or webview. |
| `database_id` | body | `string` | no | Required when validation_method is database or ondevicedatabase. |
| `postback_url` | body | `string` | no | Required when validation_method is postback. |
| `service_name` | body | `string` | no | Optional name for the new service. |
| `description` | body | `string` | no | Optional service description or webview HTML/URL. |
