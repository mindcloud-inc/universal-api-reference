# Execute Reporting GraphQL Query with LogMeIn

Executes a reporting GraphQL query in LogMeIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/goto-resolve-reporting/v1`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Execute Reporting GraphQL Query](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | GraphQL query string to execute against GoTo Resolve reporting. |
| `variables` | body | `object` | no | Optional GraphQL variables object. |
