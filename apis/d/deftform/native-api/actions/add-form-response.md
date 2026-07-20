# Add Form Response with Deftform

Creates a form response in Deftform.

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/:formId/response`
- **Base URL:** `https://deftform.com/api/v1`
- **Official documentation:** [Add Form Response](https://help.deftform.com/api/endpoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The Deftform form ID that should receive the new response. |
| `data` | body | `object` | yes | Object mapping Deftform field UUIDs to string or integer response values. |
