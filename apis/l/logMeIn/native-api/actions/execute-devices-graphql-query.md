# Execute Devices GraphQL Query with LogMeIn

Executes a devices GraphQL query in LogMeIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/goto-resolve-devices/v1`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Execute Devices GraphQL Query](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | GraphQL query string to execute against GoTo Resolve devices. |
| `variables` | body | `object` | no | Optional GraphQL variables object. |
