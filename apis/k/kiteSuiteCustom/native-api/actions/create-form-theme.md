# Create Form Theme with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/form/theme`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Create Form Theme](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `formDesign` | body | `string` | yes | ID of the form design to use as template |
| `themeName` | body | `string` | yes | Name of the theme |
| `previewImage` | body | `object` | yes | — |
