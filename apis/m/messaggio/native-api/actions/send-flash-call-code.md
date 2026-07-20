# Send Flash Call Code with Messaggio

Creates a flash call code in Messaggio.

## Endpoint

- **Method:** `POST`
- **Path:** `/send`
- **Base URL:** `https://msg.messaggio.com/api/v1`
- **Official documentation:** [Send Flash Call Code](https://messaggio.com/api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipientPhone` | body | `string` | yes | Recipient phone number in international format without a plus sign. |
| `senderCode` | body | `string` | yes | Flash Call sender code from the Messaggio project. |
| `verificationCode` | body | `string` | yes | Four-digit numeric code to deliver through Flash Call. Maximum length: 4. |
