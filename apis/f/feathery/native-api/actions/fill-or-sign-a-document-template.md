# Fill or Sign a Document Template with Feathery

## Endpoint

- **Method:** `POST`
- **Path:** `/api/document/fill/`
- **Base URL:** `https://api.feathery.io`
- **Official documentation:** [Fill or Sign a Document Template](https://api-docs.feathery.io/#fill-or-sign-a-document-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | body | `string` | yes | The ID of the document to fill. |
| `field_values` | body | `object` | no | A mapping of document field IDs to values. |
| `signer_email` | body | `string` | no | Email address to route the document to for signature after filling. |
| `user_id` | body | `string` | no | Associate an existing Feathery user with the generated document. |
