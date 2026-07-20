# Add Sequence Recipient with Hunter

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/:campaignId/recipients`
- **Base URL:** `https://api.hunter.io/v2`
- **Official documentation:** [Add Sequence Recipient](https://hunter.io/api-documentation/v2#create-recipient)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | Identifier of the sequence. |
| `emails` | body | `list<string>` | no | Email addresses to add to the sequence. |
| `lead_ids` | body | `list<string>` | no | — |
