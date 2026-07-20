# Create Webhook with FuseDesk

Creates a new webhook in FuseDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/webhooks`
- **Base URL:** `https://{appName}.fusedesk.com`
- **Official documentation:** [Create Webhook](https://documenter.getpostman.com/view/11014835/SztBc8ix#74bd4635-69aa-477c-8ba8-dbe07422af4e)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | body | `string` | yes | Webhook action to subscribe to. |
| `objectType` | body | `string` | yes | Webhook object type. |
| `url` | body | `string` | yes | Webhook target URL. |
