# Create Form Submission with Moxie

Creates a new form submission in Moxie.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/formSubmissions/create`
- **Base URL:** `https://pod01.withmoxie.com/api/public`
- **Official documentation:** [Create Form Submission](https://help.withmoxie.com/en/articles/8160298-create-form-submission)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formName` | body | `string` | no | Form name to submit. |
| `firstName` | body | `string` | no | Lead first name. |
| `lastName` | body | `string` | no | Lead last name. |
| `email` | body | `string` | no | Lead email address. |
| `phone` | body | `string` | no | Lead phone number. |
| `businessName` | body | `string` | no | Business name from the form submission. |
| `pipelineStageName` | body | `string` | no | Pipeline stage name for the submission. |
| `answers` | body | `list<object>` | no | List of answer objects for form questions. |
