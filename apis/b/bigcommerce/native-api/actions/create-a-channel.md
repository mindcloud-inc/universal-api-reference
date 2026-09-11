# Create a Channel with BigCommerce

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/channels`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `is_listable_from_ui` | body | `boolean` | no | — |
| `is_visible` | body | `boolean` | no | — |
| `platform` | body | `string` | yes | — |
| `status` | body | `list` | no | Accepted values: `active`, `archived`, `connected`, `deleted`, `disconnected`, `inactive`, `prelaunch`, `terminated`. |
| `type` | body | `list` | yes | — |
| `name` | body | `string` | yes | — |
| `external_id` | body | `string` | no | — |
