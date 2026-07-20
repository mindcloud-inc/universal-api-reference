# Create Deal with BoardCRM

Creates a new deal in BoardCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/offer/create`
- **Base URL:** `https://api.boardcrm.io/api`
- **Official documentation:** [Create Deal](https://dev.boardcrm.io/public/0.1/methods/offer#create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `column_id` | body | `number` | no | Deal column ID. |
| `lead_id` | body | `number` | no | Existing lead ID to attach to the deal. |
| `name` | body | `string` | no | Name for a new lead created together with the deal. |
| `email` | body | `string` | no | Email for a new lead created together with the deal. |
| `title` | body | `string` | no | Title field value for the new deal. |
| `description` | body | `string` | no | Description field value for the new deal. |
| `deadline` | body | `string` | no | Deal deadline in BoardCRM datetime format. |
