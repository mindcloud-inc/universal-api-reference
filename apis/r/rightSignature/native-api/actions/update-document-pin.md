# Update Document PIN with RightSignature

Updates the PIN for an existing RightSignature document.

## Endpoint

- **Method:** `PUT`
- **Path:** `/documents/:id/update_pin`
- **Base URL:** `https://api.rightsignature.com/public/v2`
- **Official documentation:** [Update Document PIN](https://api.rightsignature.com/documentation/resources/v2/documents/update_pin.en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pin` | body | `string` | yes | Document pin. Must be between 10000 and 99999 |
| `id` | path | `string` | yes | Id value |
