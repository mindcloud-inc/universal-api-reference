# Mark Check as Cleared with OnlineCheckWriter

Marks a specific check as cleared.

## Endpoint

- **Method:** `POST`
- **Path:** `/checks/:checkId/mark-as-cleared`
- **Base URL:** `https://test.onlinecheckwriter.com/api/v3`
- **Official documentation:** [Mark Check as Cleared](https://apiv3.onlinecheckwriter.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checkId` | path | `string` | yes | The check identifier. |
