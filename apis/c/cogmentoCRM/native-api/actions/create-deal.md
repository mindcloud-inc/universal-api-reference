# Create Deal with Cogmento CRM

## Endpoint

- **Method:** `POST`
- **Path:** `/deals/`
- **Base URL:** `https://api.freecrm.com/api/1`
- **Official documentation:** [Create Deal](https://api.cogmento.com/static/swagger/index.html#/Deals/post_deals_)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The title of the deal. |
| `description` | body | `string` | no | A description of the deal. |
| `assigned_to[]` | body | `array<object>` | no | Array of assignee user reference objects. |
| `tags[]` | body | `array<string>` | no | Tags associated with the deal. Send multiple values as a array. |
| `close_date` | body | `date` | no | Date the deal was completed, formatted YYYY-MM-DD. |
| `products[]` | body | `array<object>` | no | Array of product reference objects associated with the deal. |
| `amount` | body | `number` | no | Final deal value. |
