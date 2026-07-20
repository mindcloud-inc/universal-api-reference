# Generate Template with ApproveThis

Creates an approval template from JSON data in ApproveThis.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates/generate`
- **Base URL:** `https://app.approvethis.com/api/v1`
- **Official documentation:** [Generate Template](https://app.approvethis.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | An object containing template, page, and fields definitions. |
