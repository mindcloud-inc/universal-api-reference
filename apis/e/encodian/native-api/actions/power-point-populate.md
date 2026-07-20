# PowerPoint Populate with Encodian

Populates a PowerPoint file in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PowerPoint/PopulatePowerPoint`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PowerPoint Populate](https://support.encodian.com/hc/en-gb/articles/9715390966300)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | A Base64 encoded representation of the PowerPoint file to be processed |
| `jsonData` | body | `string` | yes | A JSON string containing the data used to populate template tokens |
| `jsonParseMode` | body | `string` | no | Set how JSON data should be parsed |
| `allowMissingMembers` | body | `boolean` | no | Set whether missing token values should be ignored |
| `inlineErrorMessages` | body | `boolean` | no | Set whether token errors should be written inline in the document |
| `removeEmptyParagraphs` | body | `boolean` | no | Set whether empty paragraphs should be removed |
| `dateTimeFormat` | body | `string` | no | Optional JSON mapping for custom date and time formats |
| `multipleSlides` | body | `boolean` | no | Set whether array data should duplicate slides for repeated items |
| `cultureName` | body | `string` | no | Set the culture used when processing values |
