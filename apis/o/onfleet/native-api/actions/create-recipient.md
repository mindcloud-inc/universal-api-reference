# Create Recipient with Onfleet

Creates a new recipient in Onfleet.

## Endpoint

- **Method:** `POST`
- **Path:** `/recipients`
- **Base URL:** `https://onfleet.com/api/v2`
- **Official documentation:** [Create Recipient](https://docs.onfleet.com/reference/create-recipient)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The recipient's complete name. |
| `phone` | body | `string` | yes | The recipient's phone number. |
| `notes` | body | `string` | no | Optional notes for this recipient. |
| `skipSMSNotifications` | body | `boolean` | no | Whether this recipient should skip SMS notifications. |
| `skipPhoneNumberValidation` | body | `boolean` | no | Whether to skip phone number validation for this recipient. |
| `useLongCodeForText` | body | `boolean` | no | Whether to use a toll-free long code number for SMS communication. |
