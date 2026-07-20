# Save email as draft with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/instant-emails/save-as-draft/{emailId}`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Save email as draft](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailId` | path | `string` | yes | ID of the email to save as draft |
| `subject` | body | `string` | yes | — |
| `body` | body | `string` | yes | — |
| `typeOfMail` | body | `string` | yes | — |
| `emailInterval` | body | `number` | yes | — |
| `replyTo` | body | `string` | yes | — |
| `from` | body | `string` | yes | — |
| `groups[]` | body | `array<string>` | yes | Send multiple values as a array. |
