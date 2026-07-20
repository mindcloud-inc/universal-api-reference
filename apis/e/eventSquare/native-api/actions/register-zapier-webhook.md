# Register Zapier Webhook with EventSquare

Registers a Zapier webhook in EventSquare.

## Endpoint

- **Method:** `POST`
- **Path:** `/1.0/integrations/zapier/triggers`
- **Base URL:** `https://api.eventsquare.io`
- **Official documentation:** [Register Zapier Webhook](https://api.eventsquare.io/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | The EventSquare trigger type to register a webhook for. Accepted values: `0`. |
| `url` | body | `string` | yes | The public URL EventSquare should call when the selected trigger fires. |
