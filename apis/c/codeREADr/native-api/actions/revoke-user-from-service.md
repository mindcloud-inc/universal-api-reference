# Revoke User from Service with CodeREADr

Revokes an app user's access to a scanning service in CodeREADr.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/`
- **Base URL:** `https://api.codereadr.com`
- **Official documentation:** [Revoke User from Service](https://secure.codereadr.com/apidocs/Services.md#authorize)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `service_id` | body | `string` | yes | Service or services to revoke the user from. |
| `user_id` | body | `string` | yes | User or users to revoke from the service. |
