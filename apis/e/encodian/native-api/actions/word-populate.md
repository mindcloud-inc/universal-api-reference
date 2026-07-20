# Word Populate with Encodian

Populates a Word document in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Word/PopulateWordDocument`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Word Populate](https://support.encodian.com/hc/en-gb/articles/360019620578-Populate-Word-Document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | The Microsoft Word document (DOCX) to populate. |
| `documentData` | body | `string` | yes | The JSON data to populate the document with. |
| `jsonParseMode` | body | `string` | no | Sets how JSON simple values are parsed. |
| `allowMissingValues` | body | `boolean` | no | Allow missing values within the document data. |
| `removeEmptyParagraphs` | body | `boolean` | no | Automatically remove empty paragraphs upon execution. |
| `inlineErrors` | body | `boolean` | no | Produce errors within the resultant document instead of returning an HTTP 4xx response. |
| `dateTimeFormats` | body | `string` | no | One or more specific formats for parsing DateTime values. |
| `cultureName` | body | `string` | no | Set the culture for the document prior to conversion. |
| `timeZone` | body | `string` | no | Set a specific time zone for date and time processing. |
