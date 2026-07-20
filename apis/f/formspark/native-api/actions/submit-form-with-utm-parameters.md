# Submit Form With UTM Parameters with Formspark

Creates a Formspark form submission with UTM tracking parameters.

## Endpoint

- **Method:** `POST`
- **Path:** `:formId`
- **Base URL:** `https://submit-form.com/`
- **Official documentation:** [Submit Form With UTM Parameters](https://documentation.formspark.io/integration/utm-parameters.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The Formspark form ID or the special `echo` endpoint for validation. |
| `message` | body | `string` | no | Optional message field to include in the submission body. |
| `utm_source` | body | `string` | no | UTM source attribution value. |
| `utm_medium` | body | `string` | no | UTM medium attribution value. |
| `utm_campaign` | body | `string` | no | UTM campaign attribution value. |
| `ref` | body | `string` | no | Custom referral source field supported by Formtrack. |
| `referrer` | body | `string` | no | Custom referrer field supported by Formtrack. |
