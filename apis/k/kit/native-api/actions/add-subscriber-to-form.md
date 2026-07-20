# Add Subscriber to Form with Kit

Adds an existing subscriber to a Kit form.

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/:form_id/subscribers`
- **Base URL:** `https://api.kit.com/v4`
- **Official documentation:** [Add Subscriber to Form](https://developers.kit.com/api-reference/forms/add-subscriber-to-form-by-email-address)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `number` | yes | The ID of the form to add the subscriber to. |
| `email_address` | body | `string` | yes | Email address of an existing subscriber. |
| `referrer` | body | `string` | no | Optional referrer URL to attribute this subscription. |
