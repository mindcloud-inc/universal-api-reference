# Convert Word To PDF Form with Encodian

Converts Word to a PDF form in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Conversion/WordToPdfForm`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Convert Word To PDF Form](https://support.encodian.com/hc/en-gb/articles/360012307133)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputFilename` | body | `string` | yes | The filename to assign to the resulting PDF document. |
| `filename` | body | `string` | yes | The filename including extension of the file to be converted. |
| `fileContent` | body | `string` | yes | The base64 encoded representation of the file to be converted. |
| `returnFile` | body | `boolean` | no | Set whether the action returns a file or an operation ID. |
