# Abort Multipart Upload with Discourse

Aborts a multipart upload in Discourse.

## Endpoint

- **Method:** `POST`
- **Path:** `/uploads/abort-multipart.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Abort Multipart Upload](https://docs.discourse.org/#tag/Uploads/operation/abortMultipart)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `external_upload_identifier` | body | `string` | yes | Multipart upload identifier from the external storage provider. |
