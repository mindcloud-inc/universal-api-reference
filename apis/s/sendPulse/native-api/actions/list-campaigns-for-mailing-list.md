# List Campaigns For Mailing List with SendPulse

Retrieves campaigns for a SendPulse mailing list.

## Endpoint

- **Method:** `GET`
- **Path:** `/addressbooks/:mailingListId/campaigns`
- **Base URL:** `https://api.sendpulse.com`
- **Official documentation:** [List Campaigns For Mailing List](https://sendpulse.com/integrations/api/bulk-email#campaigns-list_book)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mailingListId` | path | `string` | yes | The SendPulse mailing list identifier. |
