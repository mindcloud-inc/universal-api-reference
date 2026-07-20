# Edit Contact Tag with Cakemail

Updates an existing contact tag in Cakemail.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tags/:tag`
- **Base URL:** `https://api.cakemail.dev`
- **Official documentation:** [Edit Contact Tag](https://cakemail.dev/en/api/tags#edit-a-contact-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag` | path | `string` | yes | Current contact tag name. |
| `tag` | body | `string` | yes | New contact tag name. |
