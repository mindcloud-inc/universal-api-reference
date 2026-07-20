# Add Emails to Mailing List with SendPulse

Creates subscribers in a SendPulse mailing list.

## Endpoint

- **Method:** `POST`
- **Path:** `/addressbooks/:mailingListId/emails`
- **Base URL:** `https://api.sendpulse.com`
- **Official documentation:** [Add Emails to Mailing List](https://sendpulse.com/integrations/api/bulk-email#add-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mailingListId` | path | `string` | yes | The SendPulse mailing list identifier. |
| `emails[]` | body | `array<string>` | yes | Email addresses to add to the mailing list. |
