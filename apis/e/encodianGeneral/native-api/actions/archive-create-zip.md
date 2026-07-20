# Archive Create ZIP with Encodian - General

Creates a ZIP archive from files in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/General/AddToZip`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Archive Create ZIP](https://support.encodian.com/hc/en-gb/articles/360002674918-Add-to-Archive-ZIP)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputFilename` | body | `string` | yes | Name of the generated archive file. |
| `Documents` | body | `list<object>` | yes | Array of files to add to the archive. Each item should include fileName and fileContent. |
