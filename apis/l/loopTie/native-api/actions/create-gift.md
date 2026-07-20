# Create Gift with Loop & Tie

Creates a new gift in Loop & Tie.

## Endpoint

- **Method:** `POST`
- **Path:** `/teams/:teamId/gifts`
- **Base URL:** `https://api.loopandtie.com/v1`
- **Official documentation:** [Create Gift](https://docs.loopandtie.com/reference/teamsteam_idgifts-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gift[collection_id]` | query | `string` | no | Collection to gift. |
| `gift[collection]` | query | `string` | no | Collection name, such as $50. |
| `gift[delivery_method]` | query | `string` | no | Delivery method, such as link or email. |
| `gift[email]` | query | `string` | no | Recipient email address. |
| `gift[from_name]` | query | `string` | no | Sender display name. |
| `gift[from]` | query | `string` | no | Sender name shown to the recipient. |
| `gift[message]` | query | `string` | no | Gift message. |
| `gift[name]` | query | `string` | no | Recipient display name. |
| `teamId` | path | `string` | no | The Loop & Tie team ID. |
