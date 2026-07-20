# Update Deal with BoardCRM

Updates an existing deal in BoardCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/offer/update`
- **Base URL:** `https://api.boardcrm.io/api`
- **Official documentation:** [Update Deal](https://dev.boardcrm.io/public/0.1/methods/offer#update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | Deal ID. |
| `column_id` | body | `number` | no | Target column ID. |
| `reason_id` | body | `number` | no | Reason ID for a closed deal. |
| `deadline` | body | `string` | no | Deal deadline in BoardCRM datetime format. |
| `deadline_done` | body | `string` | no | Deadline completion flag. |
| `name` | body | `string` | no | Updated lead name. |
| `email` | body | `string` | no | Updated lead email. |
| `title` | body | `string` | no | Updated deal title. |
| `description` | body | `string` | no | Updated deal description. |
