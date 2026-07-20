# Create Collection Images with Stencil

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/collections`
- **Base URL:** `https://api.usestencil.com`
- **Official documentation:** [Create Collection Images](https://docs.usestencil.com/api/endpoints/collections#create-images-from-a-template-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | body | `string` | no | Collection ID. |
| `metadata` | body | `object` | no | Additional metadata returned with the result. |
| `modifications[]` | body | `array<object>` | no | Array of modifications applied to the collection output. |
| `select` | body | `number` | no | Number of templates to select randomly from the collection. |
| `webhook_url` | body | `string` | no | Webhook URL called when collection images are ready. |
