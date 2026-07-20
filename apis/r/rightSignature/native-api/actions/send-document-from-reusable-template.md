# Send Document From Reusable Template with RightSignature

Sends a document from a RightSignature reusable template.

## Endpoint

- **Method:** `POST`
- **Path:** `/reusable_templates/:id/send_document`
- **Base URL:** `https://api.rightsignature.com/public/v2`
- **Official documentation:** [Send Document From Reusable Template](https://api.rightsignature.com/documentation/resources/v2/reusable_templates/send_document.en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | A name for the document you are sending |
| `shared_with` | body | `list<string>` | no | List of email recipients to share the document with |
| `message` | body | `string` | no | A message for all signers |
| `in_person` | body | `boolean` | no | Whether the document should be signed in person |
| `callback_url` | body | `string` | no | Document callback url. The URL will receive a POST for each of the following document events: created , viewed , signed , executed , voided , declined . Note that due to the asynchronous nature of processing, the order in which the document callbacks are sent is not guaranteed. Only HTTP ports 80, 8000-8099, 3000-3009 and HTTPS port 443 is supported. Basic auth is also supported. Ex. “ me:pass@yourhost.example:8001/callback ”. ex. callback when document is viewed { "callbackType":"Document", "id":"edc7823a-7b99-45d7-9c3c-c7dc81f8dbf2", "event":"viewed", "documentState":"pending", "createdAt":"2016-11-14T13:45:23.199-08:00" } |
| `roles` | body | `list<object>` | yes | Document signers |
| `roles[name]` | body | `string` | yes | Role name. For text tags, the role name in the request must correspond to the recipient name given as the second argument (name) in the text tag. When signer sequencing is enabled, the role name must match the signer name set on the template. |
| `roles[signer_name]` | body | `string` | no | Signer name |
| `roles[signer_email]` | body | `string` | no | Signer email |
| `roles[signer_omitted]` | body | `boolean` | no | A signer can be omitted if set to true and if signer_sequencing is enabled |
| `roles[is_sender]` | body | `boolean` | no | Is signer the owner of document? |
| `roles[message]` | body | `string` | no | Custom message to signer. |
| `merge_field_identifier` | body | `string` | no | Merge Field Identifier. By specifying it to “name” API user can map merge field value with the name instead of merge field id |
| `merge_field_values` | body | `list<object>` | no | Merge Fields |
| `merge_field_values[id]` | path | `string` | no | Merge Field ID |
| `merge_field_values[name]` | body | `string` | no | Merge Field Name. This is the name provided to the merge field on the webapp, while creating the template. If it matches more than one merge field component in template all of them will be filled with the same value |
| `merge_field_values[value]` | body | `string` | yes | Merge Field value. If the merge field is a date, the value should be in yyyy/mm/dd or yyyy-mm-dd format. |
| `expires_in` | body | `string` | yes | Document expiration. Must be between 1 and 365 days |
| `pin` | body | `string` | no | Document pin. Must be between 10000 and 99999 |
| `tags` | body | `string` | no | Optional key value tags for categorization |
| `kba` | body | `boolean` | no | Enable KBA on the document (applicable for KBA enabled plans) |
| `id` | path | `string` | yes | Merge Field ID |
