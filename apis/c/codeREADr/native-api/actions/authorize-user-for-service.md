# Authorize User for Service with CodeREADr

Authorizes an app user for a scanning service in CodeREADr.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/`
- **Base URL:** `https://api.codereadr.com`
- **Official documentation:** [Authorize User for Service](https://secure.codereadr.com/apidocs/Services.md#authorize)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `service_id` | body | `string` | yes | Service or services to authorize the user for. |
| `user_id` | body | `string` | yes | User or users to authorize for the service. |
