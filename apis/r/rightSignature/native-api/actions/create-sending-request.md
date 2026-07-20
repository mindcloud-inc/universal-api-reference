# Create Sending Request with RightSignature

Creates a RightSignature sending request for a one-off document.

## Endpoint

- **Method:** `POST`
- **Path:** `/sending_requests`
- **Base URL:** `https://api.rightsignature.com/public/v2`
- **Official documentation:** [Create Sending Request](https://api.rightsignature.com/documentation/resources/v2/sending_requests/create.en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `object` | yes | Upload file information |
| `file[name]` | body | `string` | yes | Filename withe extension |
| `file[source]` | body | `string` | yes | Source of file. Only 'upload' is supported. |
| `document` | body | `object` | yes | Document information |
| `document[name]` | body | `string` | yes | Document name |
| `document[signer_sequencing]` | body | `boolean` | yes | Send to signers in specified sequence. |
| `document[personalized_messages]` | body | `boolean` | no | Use custom messages per signer. Specified in 'roles' attribute. |
| `document[shared_with]` | body | `list<string>` | no | Array of emails to CC document. |
| `document[identity_method]` | body | `string` | no | How to authenticate signers (email \| none). |
| `document[callback_url]` | body | `string` | no | Document callback url. The URL will receive a POST for each of the following document events: created , viewed , signed , executed , voided , declined . Note that due to the asynchronous nature of processing, the order in which the document callbacks are sent is not guaranteed. Only HTTP ports 80, 8000-8099, 3000-3009 and HTTPS port 443 is supported. Basic auth is also supported. Ex. “ me:pass@yourhost.example:8001/callback ”. Note : This is different from the sending request callback url which receives status updates regarding the sending request itself. ex. callback when document is viewed { "callbackType": "Document" , "id": "edc7823a-7b99-45d7-9c3c-c7dc81f8dbf2" , "event": "viewed" , "documentState": "pending" , "createdAt": "2016-11-14T13:45:23.199-08:00" } |
| `document[api_embedded]` | body | `boolean` | no | Whether the document should be embedded. |
| `document[api_embed_width]` | body | `string` | no | Embed width |
| `document[api_embed_height]` | body | `string` | no | Embed height |
| `document[roles]` | body | `list<object>` | yes | Document signers |
| `document[roles][name]` | body | `string` | yes | Role name. For text tags, the role name in the request must correspond to the recipient name given as the second argument (name) in the text tag. When signer sequencing is enabled, the role name must match the signer name set on the template. |
| `document[roles][signer_name]` | body | `string` | yes | Signer name |
| `document[roles][is_sender]` | body | `boolean` | no | Is signer the owner of document? |
| `document[roles][sequence]` | body | `number` | no | Signer order (starting at 0), required if signer_sequencing is enabled. |
| `document[roles][message]` | body | `string` | no | Custom message to signer. |
| `document[roles][signer_email]` | body | `string` | yes | Signer email |
| `document[expires_in]` | body | `string` | yes | Document expiration. Must be between 1 and 365 days |
| `document[pin]` | body | `string` | no | Document pin. Must be between 10000 and 99999 |
| `document[tags]` | body | `string` | no | Optional key value tags for categorization |
| `document[kba]` | body | `boolean` | no | Enable KBA on the document (applicable for KBA enabled plans) |
| `callback_url` | body | `string` | no | URL to receive sending request status updates. The URL will receive a POST when the sending request is sent as a document or an error occured in processing. Only HTTP ports 80, 8000-8099, 3000-3009 and HTTPS port 443 is supported. Basic auth is also supported. Ex. value: “ me:pass@yourhost.example/req_callback ” ex. callback when successful { "sending_request": { "id": "09001350-1853-471c-955a-abb7d3120aa1", "status": "completed", "document_template_id": "733816f6-939f-4a8d-98de-55e357ab07d4", "created_at":"2016-08-10T18:57:29.400-07:00", "updated_at":"2016-08-10T19:05:11.100-07:00" } } ex. callback when processing fails { "sending_request": { "id": "09001350-1853-471c-955a-abb7d3120aa1", "status": "errored", "status_message": "File was password protected" "document_template_id": null, "created_at":"2016-08-10T18:57:29.400-07:00", "updated_at":"2016-08-10T19:05:11.100-07:00" } } |
