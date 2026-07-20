# Delete Make Webhook with EventSquare

Deletes a Make webhook from EventSquare.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/1.0/integrations/make/triggers`
- **Base URL:** `https://api.eventsquare.io`
- **Official documentation:** [Delete Make Webhook](https://api.eventsquare.io/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | The EventSquare trigger type for the webhook you want to delete. Accepted values: `0`. |
| `url` | body | `string` | yes | The exact webhook URL to remove from EventSquare. |
