# Replace All Text with Google Docs

Replaces matching text in a Google Docs document.

## Endpoint

- **Method:** `POST`
- **Path:** `/[:documentId]\:batchUpdate`
- **Base URL:** `https://docs.googleapis.com/v1/documents`
- **Official documentation:** [Replace All Text](https://developers.google.com/workspace/docs/api/reference/rest/v1/documents/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `list<string>` | yes | ID of the document to update |
| `requests[0].replaceAllText.containsText.text` | body | `string` | yes | Text to find |
| `requests[0].replaceAllText.replaceText` | body | `string` | yes | Replacement text |
| `requests[0].replaceAllText.containsText.matchCase` | body | `boolean` | no | Whether text matching should be case-sensitive |
