# Renew Form Watch with Google Forms

Renews a form watch in Google Forms for seven days.

## Endpoint

- **Method:** `POST`
- **Path:** `/:formId/watches/:watchId:renew`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Renew Form Watch](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms.watches/renew)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier. |
| `watchId` | path | `string` | yes | The watch identifier. |
