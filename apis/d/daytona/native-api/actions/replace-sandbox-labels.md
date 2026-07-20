# Replace Sandbox Labels with Daytona

Replaces sandbox labels in Daytona.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sandbox/[:sandboxIdOrName]/labels`
- **Base URL:** `https://app.daytona.io/api`
- **Official documentation:** [Replace Sandbox Labels](https://www.daytona.io/docs/tools/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sandboxIdOrName` | path | `string` | yes | ID or name of the sandbox. |
| `labels` | body | `object` | yes | Key-value pairs of labels. |
