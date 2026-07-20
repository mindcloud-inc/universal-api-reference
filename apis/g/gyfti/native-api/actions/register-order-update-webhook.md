# Register Order Update Webhook with gyfti

Registers an order update webhook in gyfti.

## Endpoint

- **Method:** `POST`
- **Path:** `/wf/new_hook_order_update/`
- **Base URL:** `https://app.gyfti.fr/api/1.1`
- **Official documentation:** [Register Order Update Webhook](https://developer.gyfti.fr/retrieve-data-from-campaigns/order-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hookUrl` | body | `string` | yes | Destination URL that gyfti should call when an order update occurs. |
| `user` | body | `string` | yes | gyfti user email associated with the webhook registration. |
