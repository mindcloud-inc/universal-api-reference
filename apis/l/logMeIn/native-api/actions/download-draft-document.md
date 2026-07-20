# Download Draft Document with LogMeIn

Downloads a draft document from LogMeIn.

## Endpoint

- **Method:** `GET`
- **Path:** `/resolve/knowledge-base/v2/drafts/:draftId/download`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Download Draft Document](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `draftId` | path | `string` | yes | Required draft ID to download. |
| `inline` | query | `boolean` | no | Whether to display the file inline instead of downloading. |
