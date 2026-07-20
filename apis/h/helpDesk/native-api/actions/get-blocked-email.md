# Get Blocked Email with HelpDesk

Retrieves a blocked email from HelpDesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/blockedEmails/:blockedEmailID`
- **Base URL:** `https://api.helpdesk.com`
- **Official documentation:** [Get Blocked Email](https://api.helpdesk.com/docs#tag/Spam-management/operation/blockedEmailsRead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blockedEmailID` | path | `string` | yes | The HelpDesk blocked email ID. |
