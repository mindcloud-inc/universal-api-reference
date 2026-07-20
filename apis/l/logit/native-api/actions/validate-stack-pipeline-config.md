# Validate Stack Pipeline Config with Logit

Validates stack pipeline config in Logit.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/stacks/:stackId/pipeline-config/validation`
- **Base URL:** `https://dashboard.logit.io`
- **Official documentation:** [Validate Stack Pipeline Config](https://logit.io/docs/developer-api/pipeline-configuration/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `stackId` | path | `string` | yes |
| `testConfiguration` | body | `string` | yes |
