# Remove Contact From Sequence with Reply

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/actions/removepersonfromcampaignbyid`
- **Base URL:** `https://api.reply.io`
- **Official documentation:** [Remove Contact From Sequence](https://apidocs.reply.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | body | `number` | yes | Reply campaign identifier. |
| `email` | body | `string` | yes | Contact email to remove from the sequence. |
