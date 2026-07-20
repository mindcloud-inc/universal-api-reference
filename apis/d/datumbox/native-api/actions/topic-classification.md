# Topic Classification with Datumbox

Classifies a document's topic in Datumbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/TopicClassification.json`
- **Base URL:** `http://api.datumbox.com/1.0`
- **Official documentation:** [Topic Classification](https://www.datumbox.com/files/API-Documentation-1.0v.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The clear text to classify by topic. |
