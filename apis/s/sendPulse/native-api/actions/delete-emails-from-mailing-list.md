# Delete Emails From Mailing List with SendPulse

Deletes subscribers from a SendPulse mailing list.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/addressbooks/:mailingListId/emails`
- **Base URL:** `https://api.sendpulse.com`
- **Official documentation:** [Delete Emails From Mailing List](https://sendpulse.com/integrations/api/bulk-email#delete-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mailingListId` | path | `string` | yes | The SendPulse mailing list identifier. |
| `emails[]` | body | `array<string>` | yes | Email addresses to remove from the mailing list. |
