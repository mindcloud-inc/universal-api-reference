# Create Attachment Link with vPlan

## Endpoint

- **Method:** `POST`
- **Path:** `/collection/[:collection_id]/attachment`
- **Base URL:** `https://api.vplan.com/v1`
- **Official documentation:** [Create Attachment Link](https://docs.api.vplan.com/attachment_create_link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `card_id` | body | `string` | no | Optional card to attach the link to. |
| `collection_id` | path | `string` | yes | — |
| `type` | body | `string` | no | Attachment provider/type label. |
| `filename` | body | `string` | yes | Attachment filename. |
| `file` | body | `string` | yes | Public URL for the attachment link. |
