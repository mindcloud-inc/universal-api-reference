# Create Deal Comment with BoardCRM

Creates a new comment for a deal in BoardCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/comment/create`
- **Base URL:** `https://api.boardcrm.io/api`
- **Official documentation:** [Create Deal Comment](https://dev.boardcrm.io/public/0.1/methods/comment#create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offer_id` | body | `number` | yes | Deal ID to attach the comment to. |
| `text` | body | `string` | no | Comment text between 1 and 2500 characters. |
