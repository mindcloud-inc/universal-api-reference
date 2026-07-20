# Get Mailbox Insight with DitLead

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/mailbox/insight/{mailboxId}`
- **Base URL:** `https://api.ditlead.com`
- **Official documentation:** [Get Mailbox Insight](https://ditlead.com/developer/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fromDate` | body | `date` | no | — |
| `mailboxId` | path | `string` | yes | Public ID of the mailbox. |
| `toDate` | body | `date` | no | — |
