# Push Contact To Sequence with Reply

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/actions/pushtocampaign`
- **Base URL:** `https://api.reply.io`
- **Official documentation:** [Push Contact To Sequence](https://apidocs.reply.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | body | `number` | yes | Reply campaign identifier. |
| `email` | body | `string` | yes | Contact email to enroll in the sequence. |
