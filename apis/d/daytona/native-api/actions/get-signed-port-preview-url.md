# Get Signed Port Preview URL with Daytona

Retrieves a signed sandbox port preview URL from Daytona.

## Endpoint

- **Method:** `GET`
- **Path:** `/sandbox/[:sandboxIdOrName]/ports/[:port]/signed-preview-url`
- **Base URL:** `https://app.daytona.io/api`
- **Official documentation:** [Get Signed Port Preview URL](https://www.daytona.io/docs/tools/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sandboxIdOrName` | path | `string` | yes | ID or name of the sandbox. |
| `port` | path | `number` | yes | Port number to get signed preview URL for. |
