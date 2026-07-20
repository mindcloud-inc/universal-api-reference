# Start Batch Verification with Kickbox

Starts a batch email verification job in Kickbox.

## Endpoint

- **Method:** `PUT`
- **Path:** `/verify-batch`
- **Base URL:** `https://api.kickbox.com/v2`
- **Official documentation:** [Start Batch Verification](https://docs.kickbox.com/docs/batch-verification-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/csv` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails` | body | `string` | yes | Plain-text or CSV body content containing one email address per line. |
