# Get Document Statistics with Smartcat

Retrieves document statistics from the Smartcat account.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/integration/v1/document/statistics`
- **Base URL:** `https://smartcat.ai`
- **Official documentation:** [Get Document Statistics](https://developers.smartcat.com/api/#fetch-statistics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | query | `string` | yes | Document ID in the format documentId_targetLanguageId |
| `onlyExactMatches` | query | `boolean` | no | Whether to count only exact translation memory matches |
