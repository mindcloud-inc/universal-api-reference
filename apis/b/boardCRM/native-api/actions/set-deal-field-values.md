# Set Deal Field Values with BoardCRM

Updates field values for a deal in BoardCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/offer/set-values`
- **Base URL:** `https://api.boardcrm.io/api`
- **Official documentation:** [Set Deal Field Values](https://dev.boardcrm.io/public/0.1/methods/offer#set-values)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | Deal ID. |
| `title` | body | `string` | no | Deal title field value. |
| `description` | body | `string` | no | Deal description field value. Pass null to clear it. |
| `price` | body | `number` | no | Deal price field value. |
