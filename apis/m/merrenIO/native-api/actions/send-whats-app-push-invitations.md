# Send WhatsApp Push Invitations with MerrenIO

## Endpoint

- **Method:** `POST`
- **Path:** `/deploy/uploadRecipent`
- **Base URL:** `https://app.merren.io`
- **Official documentation:** [Send WhatsApp Push Invitations](https://merren.io/api-integration/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | body | `string` | yes | Survey to send WhatsApp invitations for. |
| `recipientsPayload` | body | `string` | yes | Recipient data to push through Merren's WhatsApp invitation flow. |
