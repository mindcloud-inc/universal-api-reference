# Batch Edit Files And Folders with Dynalist

Updates multiple files and folders in Dynalist.

## Endpoint

- **Method:** `POST`
- **Path:** `/file/edit`
- **Base URL:** `https://dynalist.io/api/v1/`
- **Official documentation:** [Batch Edit Files And Folders](https://apidocs.dynalist.io/#make-changes-to-documents-and-folders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `changes[]` | body | `array<object>` | yes | Array of documented file-level changes to apply. |
