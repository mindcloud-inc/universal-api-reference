# Delete Zapier Webhook with EventSquare

Deletes a Zapier webhook from EventSquare.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/1.0/integrations/zapier/triggers`
- **Base URL:** `https://api.eventsquare.io`
- **Official documentation:** [Delete Zapier Webhook](https://api.eventsquare.io/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | The EventSquare trigger type for the webhook you want to delete. Accepted values: `0`. |
| `url` | body | `string` | yes | The exact webhook URL to remove from EventSquare. |
