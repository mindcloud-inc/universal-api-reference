# List Mailing List Variables with SendPulse

Retrieves variables for a SendPulse mailing list.

## Endpoint

- **Method:** `GET`
- **Path:** `/addressbooks/:mailingListId/variables`
- **Base URL:** `https://api.sendpulse.com`
- **Official documentation:** [List Mailing List Variables](https://sendpulse.com/integrations/api/bulk-email#variables)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mailingListId` | path | `string` | yes | The SendPulse mailing list identifier. |
