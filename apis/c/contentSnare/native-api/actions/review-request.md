# Review Request with Content Snare

Reviews a request field in Content Snare.

## Endpoint

- **Method:** `PUT`
- **Path:** `/partner_api/v1/fields/{id}/review`
- **Base URL:** `https://api.contentsnare.com`
- **Official documentation:** [Review Request](https://api.contentsnare.com/partner_api/v1/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Request ID. |
| `answers_attributes[]` | body | `array<object>` | no | <b>DEPRECATED</b> |
| `answers_attributes[].id` | body | `string` | no | Answer id |
| `answers_attributes[].rejection_comment` | body | `string` | no | A message for your client letting them know why you rejected the answer and what they need to do to fix it |
| `answers_attributes[].status` | body | `string` | no | Answer status. <br>Set status 'approved' for the following actions: approve. <br> status 'todo' for the following actions: remove reject, remove approval. <br>Set status 'redo' for the following actions: reject. |
| `rejection_comment` | body | `string` | no | A message for your client letting them know why you rejected the field and what they need to do to fix it |
| `status` | body | `string` | no | Field status. <br>Set status 'approved' for the following actions: approve. <br>Set status 'done' for the following actions: submit for review, remove reject, remove approval. <br>Set status 'todo' for the following actions: revise. <br>Set status 'redo' for the following actions: reject. |
