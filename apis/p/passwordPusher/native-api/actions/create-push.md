# Create Push with Password Pusher

Creates a secure push in Password Pusher.

## Endpoint

- **Method:** `POST`
- **Path:** `/pushes`
- **Base URL:** `https://eu.pwpush.com/api/v2`
- **Official documentation:** [Create Push](https://eu.pwpush.com/help/api/pushes)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `push.payload` | body | `string` | yes | The secret text to share. |
| `push.expire_after_duration` | body | `number` | no | Duration enum from 0 to 17. |
| `push.expire_after_views` | body | `number` | no | Number of views before expiration, from 1 to 100. |
| `push.kind` | body | `string` | no | Push type: text, file, url, or qr. JSON actions support text/url/qr payloads; file uploads require multipart form-data. |
| `push.passphrase` | body | `string` | no | Optional passphrase required to view the push. |
| `push.name` | body | `string` | no | Optional dashboard name for the push. |
| `push.note` | body | `string` | no | Internal note only visible to the creator. |
| `push.deletable_by_viewer` | body | `boolean` | no | Whether recipients may delete the push. |
| `push.retrieval_step` | body | `boolean` | no | Require an extra retrieval step. |
| `account_id` | body | `number` | no | Optional account ID for multi-account users. |
