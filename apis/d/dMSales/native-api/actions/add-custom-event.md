# Add Custom Event with DMSales

Creates a custom event in DMSales.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/events/add-custom-event`
- **Base URL:** `https://app.dmsales.com`
- **Official documentation:** [Add Custom Event](https://app.dmsales.com/api-doc/default)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Custom event type. |
| `base_key` | body | `string` | no | Optional contact base key. |
| `email` | body | `string` | no | Optional contact email. |
| `custom` | body | `object` | yes | Custom event payload object. |
