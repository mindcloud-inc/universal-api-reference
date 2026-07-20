# Share Document with RightSignature

Shares a document in RightSignature with new recipients.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/:id/share`
- **Base URL:** `https://api.rightsignature.com/public/v2`
- **Official documentation:** [Share Document](https://api.rightsignature.com/documentation/resources/v2/documents/share.en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shared_with` | body | `string` | yes | List of email recipients to share the document with |
| `id` | path | `string` | yes | Id value |
