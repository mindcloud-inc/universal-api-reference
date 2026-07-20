# Get Mailing List Contact Count with SendPulse

Retrieves the contact count for a SendPulse mailing list.

## Endpoint

- **Method:** `GET`
- **Path:** `/addressbooks/:mailingListId/emails/total`
- **Base URL:** `https://api.sendpulse.com`
- **Official documentation:** [Get Mailing List Contact Count](https://sendpulse.com/integrations/api/bulk-email#get_total_addresses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mailingListId` | path | `string` | yes | The SendPulse mailing list identifier. |
