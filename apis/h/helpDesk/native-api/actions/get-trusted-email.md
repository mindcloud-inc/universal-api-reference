# Get Trusted Email with HelpDesk

Retrieves a trusted email from HelpDesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/trustedEmails/:trustedEmailID`
- **Base URL:** `https://api.helpdesk.com`
- **Official documentation:** [Get Trusted Email](https://api.helpdesk.com/docs#tag/Spam-management/operation/treustedEmailRead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trustedEmailID` | path | `string` | yes | The HelpDesk trusted email ID. |
