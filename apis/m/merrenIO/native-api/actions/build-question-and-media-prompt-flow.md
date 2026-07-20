# Build Question And Media Prompt Flow with MerrenIO

## Endpoint

- **Method:** `POST`
- **Path:** `/question/applyLogic`
- **Base URL:** `https://app.merren.io`
- **Official documentation:** [Build Question And Media Prompt Flow](https://merren.io/api-integration/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `questionId` | body | `string` | yes | Question to attach logic to. |
| `logic` | body | `string` | yes | Logic payload for the flow rule. |
