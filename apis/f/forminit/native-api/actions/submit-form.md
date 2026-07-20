# Submit Form with Forminit

Creates a new submission for a Forminit form.

## Endpoint

- **Method:** `POST`
- **Path:** `/f/:formId`
- **Base URL:** `https://api.forminit.com`
- **Official documentation:** [Submit Form](https://forminit.com/docs/submit-form-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The Forminit form identifier. |
| `blocks` | body | `string<string>` | yes | JSON string containing the Forminit `blocks` array. |
