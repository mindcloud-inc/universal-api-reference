# Update Pre-Authorization Tokenization Contact Details with Payrexx

Updates pre-authorization or tokenization contact details in Payrexx.

## Endpoint

- **Method:** `PUT`
- **Path:** `Transaction/:id/`
- **Base URL:** `https://api.payrexx.com/v1.14/`
- **Official documentation:** [Update Pre-Authorization Tokenization Contact Details](https://developers.payrexx.com/reference/update-contact-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the Pre-Authorization / Tokenization. |
| `fields` | body | `object` | yes | The contact data fields which should be stored. |
