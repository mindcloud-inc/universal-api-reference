# List Form Responses with Deftform

Retrieves responses for a form from Deftform.

## Endpoint

- **Method:** `GET`
- **Path:** `/responses/:formId`
- **Base URL:** `https://deftform.com/api/v1`
- **Official documentation:** [List Form Responses](https://help.deftform.com/api/endpoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The Deftform form ID, available from the form detail page or the List Forms action. |
