# List Mailing List Emails with SendPulse

Retrieves emails from a SendPulse mailing list.

## Endpoint

- **Method:** `GET`
- **Path:** `/addressbooks/:mailingListId/emails`
- **Base URL:** `https://api.sendpulse.com`
- **Official documentation:** [List Mailing List Emails](https://sendpulse.com/integrations/api/bulk-email#lists-emails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mailingListId` | path | `string` | yes | The SendPulse mailing list identifier. |
| `limit` | query | `number` | no | Maximum number of contacts to return. |
| `offset` | query | `number` | no | Number of contacts to skip before returning results. |
| `active` | query | `boolean` | no | Filter to active contacts only. |
| `not_active` | query | `boolean` | no | Filter to inactive contacts only. |
