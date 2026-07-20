# AI Process Mortgage Document US with Encodian - General

Extracts US mortgage document data with Encodian AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/General/AIProcessMortgageUS`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [AI Process Mortgage Document US](https://support.encodian.com/hc/en-gb/articles/19808100431004)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | Base64-encoded source file content. |
| `processFileMortgageModel` | body | `string` | yes | Select the Encodian mortgage document model to use. |
