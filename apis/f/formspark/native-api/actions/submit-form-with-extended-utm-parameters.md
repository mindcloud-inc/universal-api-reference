# Submit Form With Extended UTM Parameters with Formspark

Creates a Formspark form submission with extended UTM parameters.

## Endpoint

- **Method:** `POST`
- **Path:** `:formId`
- **Base URL:** `https://submit-form.com/`
- **Official documentation:** [Submit Form With Extended UTM Parameters](https://documentation.formspark.io/integration/utm-parameters.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | Formspark form ID or the special `echo` endpoint for validation. |
| `message` | body | `string` | no | Submitted message body. |
| `utm_source` | body | `string` | yes | Traffic source. |
| `utm_medium` | body | `string` | no | Traffic medium. |
| `utm_campaign` | body | `string` | no | Campaign name. |
| `utm_term` | body | `string` | no | Paid-search keyword term. |
| `utm_content` | body | `string` | no | Ad or content variant identifier. |
