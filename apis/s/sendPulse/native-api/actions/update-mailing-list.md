# Update Mailing List with SendPulse

Updates an existing mailing list in SendPulse.

## Endpoint

- **Method:** `PUT`
- **Path:** `/addressbooks/:mailingListId`
- **Base URL:** `https://api.sendpulse.com`
- **Official documentation:** [Update Mailing List](https://sendpulse.com/integrations/api/bulk-email#edit-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mailingListId` | path | `string` | yes | The SendPulse mailing list identifier. |
| `name` | body | `string` | yes | Updated name for the mailing list. |
