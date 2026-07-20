# Edit template with Routee

Updates an existing template in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/template/edit/:id`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Edit template](https://docs.routee.net/reference/edit-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the template uploaded in the service. Use this method to get the template ID (use either real_id or id parameter from the reply) |
| `body` | body | `string` | yes | HTML version of the email, encoded in base64 |
| `lang` | body | `string` | no | language of template, two-character language code |
