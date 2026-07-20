# Import contact groups to an instant email with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/instant-emails/save-groups/{emailId}`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Import contact groups to an instant email](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailId` | path | `string` | yes | ID of the instant email to import groups into |
| `groups[]` | body | `array<string>` | yes | List of group IDs to import Send multiple values as a array. |
| `recipients[]` | body | `array<string>` | yes | List of recipient email addresses Send multiple values as a array. |
