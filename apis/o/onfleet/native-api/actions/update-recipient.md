# Update Recipient with Onfleet

Updates an existing recipient in Onfleet.

## Endpoint

- **Method:** `PUT`
- **Path:** `/recipients/:recipientId`
- **Base URL:** `https://onfleet.com/api/v2`
- **Official documentation:** [Update Recipient](https://docs.onfleet.com/reference/update-recipient)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipientId` | path | `string` | yes | The Onfleet recipient ID. |
| `name` | body | `string` | no | The recipient's complete name. |
| `notes` | body | `string` | no | Optional notes for this recipient. |
| `skipSMSNotifications` | body | `boolean` | no | Whether this recipient should skip SMS notifications. |
