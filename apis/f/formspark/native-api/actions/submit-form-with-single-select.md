# Submit Form With Single Select with Formspark

Creates a Formspark form submission with a single select value.

## Endpoint

- **Method:** `POST`
- **Path:** `:formId`
- **Base URL:** `https://submit-form.com/`
- **Official documentation:** [Submit Form With Single Select](https://documentation.formspark.io/html-form/drop-down-list.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Formspark form ID or the special `echo` endpoint for validation. |
| `car` | body | `string` | yes | Single selected drop-down value. |
