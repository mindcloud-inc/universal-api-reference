# Get Form Embedded Code with CleverReach

Retrieves deprecated embedded form code from CleverReach.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/forms.json/:id/code`
- **Base URL:** `https://rest.cleverreach.com`
- **Official documentation:** [Get Form Embedded Code](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/forms-v3.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id. |
| `badget` | query | `boolean` | no | Enable Badget (Disable only for non free plans) (default: false). |
| `embedded` | query | `boolean` | no | Embedded (default: false). |
| `js` | query | `boolean` | no | Embedded JS (default: true). |
| `css` | query | `boolean` | no | Embedded CSS (default: true). |
