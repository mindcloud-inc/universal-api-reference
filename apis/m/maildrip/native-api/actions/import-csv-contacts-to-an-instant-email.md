# Import CSV contacts to an instant email with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/instant-emails/upload/{emailId}`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Import CSV contacts to an instant email](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `draftEmailId` | path | `string` | yes | ID of the instant email to import contacts into |
| `contacts[]` | body | `array<object>` | yes | Send multiple values as a array. |
