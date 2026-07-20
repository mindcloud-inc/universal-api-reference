# Send Warming Emails with DitLead

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/mailbox/warming/send`
- **Base URL:** `https://api.ditlead.com`
- **Official documentation:** [Send Warming Emails](https://ditlead.com/developer/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mailboxAddress` | body | `string` | no | — |
| `mailboxId` | body | `string` | no | Public ID of the mailbox to warm. |
