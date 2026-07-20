# Embed Document From Reusable Template with RightSignature

Creates an embeddable document from a RightSignature reusable template.

## Endpoint

- **Method:** `POST`
- **Path:** `/reusable_templates/:id/embed_document`
- **Base URL:** `https://api.rightsignature.com/public/v2`
- **Official documentation:** [Embed Document From Reusable Template](https://api.rightsignature.com/documentation/resources/v2/reusable_templates/embed_document.en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | A name for the document you are sending |
| `shared_with` | body | `list<string>` | no | List of email recipients to share the document with |
| `message` | body | `string` | no | A message for all signers |
| `roles` | body | `list<object>` | yes | Document signers |
| `roles[name]` | body | `string` | yes | Role name. For text tags, role name must match. |
| `roles[signer_name]` | body | `string` | yes | Signer name |
| `roles[signer_email]` | body | `string` | no | Signer email. |
| `roles[is_sender]` | body | `boolean` | no | Is signer the owner of document? |
| `roles[message]` | body | `string` | no | Custom message to signer. |
| `api_embed_width` | body | `string` | yes | Embed width |
| `api_embed_height` | body | `string` | yes | Embed height |
| `merge_field_identifier` | body | `string` | no | Merge Field Identifier. By specifying it to “name” API user can map merge field value with the name instead of merge field id |
| `merge_field_values` | body | `list<object>` | no | Merge Fields |
| `merge_field_values[id]` | path | `string` | no | Merge Field ID |
| `merge_field_values[name]` | body | `string` | no | Merge Field Name. This is the name provided to the merge field on the webapp, while creating the template. If it matches more than one merge field component in template all of them will be filled with the same value |
| `merge_field_values[value]` | body | `string` | yes | Merge Field value. If the merge field is a date, the value should be in yyyy/mm/dd or yyyy-mm-dd format. |
| `expires_in` | body | `string` | yes | Document expiration. Must be between 1 and 365 days |
| `tags` | body | `string` | no | Optional key value tags for categorization |
| `id` | path | `string` | yes | Merge Field ID |
