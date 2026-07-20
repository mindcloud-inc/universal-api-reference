# Create Form Watch with Google Forms

Creates a new seven-day form watch in Google Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/:formId/watches`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Create Form Watch](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms.watches/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier. |
| `eventType` | body | `list` | yes | Watch event type. Google currently supports schema changes. Accepted values: `0`. |
| `topicName` | body | `string` | yes | Full Cloud Pub/Sub topic name that receives notifications. |
| `watchId` | body | `string` | no | Advanced: custom watch ID. Must be unused and 4-63 characters if provided. |
