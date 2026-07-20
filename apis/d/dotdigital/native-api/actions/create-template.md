# Create Template with Dotdigital

Creates a new email campaign template in Dotdigital.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/templates`
- **Base URL:** `https://r2-api.dotmailer.com`
- **Official documentation:** [Create Template](https://developer.dotdigital.com/reference/create-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the template being created |
| `subject` | body | `string` | yes | The email subject line of the template |
| `fromName` | body | `string` | yes | The from name of the template |
| `htmlContent` | body | `string` | yes | The HTML content of the template |
| `plainTextContent` | body | `string` | yes | The plain text content of the template |
