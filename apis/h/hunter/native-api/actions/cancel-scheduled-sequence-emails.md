# Cancel Scheduled Sequence Emails with Hunter

## Endpoint

- **Method:** `DELETE`
- **Path:** `/campaigns/:campaignId/recipients`
- **Base URL:** `https://api.hunter.io/v2`
- **Official documentation:** [Cancel Scheduled Sequence Emails](https://hunter.io/api-documentation/v2#cancel-scheduled-emails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | Identifier of the sequence. |
| `emails` | body | `list<string>` | yes | Email addresses whose scheduled messages should be canceled. |
