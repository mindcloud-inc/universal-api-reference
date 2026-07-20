# Authenticate with Aspire

## Endpoint

- **Method:** `POST`
- **Path:** `Authorization`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Authenticate](https://guide.youraspire.com/apidocs/authorization-7)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ClientId` | body | `string` | no |
| `Secret` | body | `string` | no |
| `environment` | body | `string` | no |
