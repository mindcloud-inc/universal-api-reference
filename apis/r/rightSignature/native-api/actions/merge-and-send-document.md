# Merge And Send Document with RightSignature

Creates and sends a document from a RightSignature reusable template.

## Endpoint

- **Method:** `POST`
- **Path:** `/reusable_templates/:id/merge_and_send_document`
- **Base URL:** `https://api.rightsignature.com/public/v2`
- **Official documentation:** [Merge And Send Document](https://api.rightsignature.com/documentation/resources/v2/reusable_templates/merge_and_send_document.en.html)

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
| `merge_field_data` | body | `object` | yes | Merge fields data |
| `expires_in` | body | `string` | no | Document expiration. Must be between 1 and 365 days |
| `expires_at` | body | `string` | no | Document expiration date time. An expires_at date time should not be earlier than the current date time, and it must be in the UTC time format. |
| `pin` | body | `string` | no | Document pin. Must be between 10000 and 99999 |
| `tags` | body | `string` | no | Optional key value tags for categorization |
| `kba` | body | `boolean` | no | Enable KBA on the document (applicable for KBA enabled plans) |
| `id` | path | `string` | yes | Id value |
