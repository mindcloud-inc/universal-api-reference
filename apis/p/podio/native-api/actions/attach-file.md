# Attach File with Podio

Attaches a file to a Podio object.

## Endpoint

- **Method:** `POST`
- **Path:** `/file/:file_id/attach`
- **Base URL:** `https://api.podio.com`
- **Official documentation:** [Attach File](https://developers.podio.com/doc/files/attach-file-22518)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | path | `string` | yes | The ID of the uploaded file to attach. |
| `ref_type` | body | `string` | yes | The type of object the file should be attached to. |
| `ref_id` | body | `number` | yes | The ID of the object the file should be attached to. |
| `silent` | query | `boolean` | no | Suppress stream bumping and notifications for the attachment. |
