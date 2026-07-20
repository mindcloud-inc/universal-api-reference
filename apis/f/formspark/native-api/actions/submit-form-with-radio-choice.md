# Submit Form With Radio Choice with Formspark

Creates a Formspark form submission with a radio choice.

## Endpoint

- **Method:** `POST`
- **Path:** `:formId`
- **Base URL:** `https://submit-form.com/`
- **Official documentation:** [Submit Form With Radio Choice](https://documentation.formspark.io/html-form/special-input-types.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Formspark form ID or the special `echo` endpoint for validation. |
| `color` | body | `string` | yes | Single selected radio value. |
