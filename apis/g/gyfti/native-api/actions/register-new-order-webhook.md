# Register New Order Webhook with gyfti

Registers a new order webhook in gyfti.

## Endpoint

- **Method:** `POST`
- **Path:** `/wf/new_hook_order/`
- **Base URL:** `https://app.gyfti.fr/api/1.1`
- **Official documentation:** [Register New Order Webhook](https://developer.gyfti.fr/retrieve-data-from-campaigns/new-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hookUrl` | body | `string` | yes | Destination URL that gyfti should call when a new order is created. |
| `user` | body | `string` | no | Optional gyfti user email associated with the webhook registration. |
