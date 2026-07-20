# Create Webhook with PlatoForms

Creates a new webhook in PlatoForms.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/form/{{form_identifier}}/`
- **Base URL:** `https://api.platoforms.com/v4`
- **Official documentation:** [Create Webhook](https://apidocs.platoforms.com/#operation/webhooks_form_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_identifier` | path | `string` | yes | — |
| `hook_url` | body | `string` | yes | Your webhook endpoint URL |
| `name` | body | `string` | no | Descriptive name for the webhook |
| `create_shared_urls` | body | `boolean` | no | Include public download URLs |
| `submit_data_as_dict` | body | `boolean` | no | Send data as dictionary format |
| `is_instant` | body | `boolean` | no | Instant delivery vs batched |
