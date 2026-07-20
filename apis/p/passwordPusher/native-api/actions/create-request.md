# Create Request with Password Pusher

Creates a secure request in Password Pusher.

## Endpoint

- **Method:** `POST`
- **Path:** `/requests`
- **Base URL:** `https://eu.pwpush.com/api/v2`
- **Official documentation:** [Create Request](https://eu.pwpush.com/help/api/requests)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request.request` | body | `string` | yes | The request text or message to share. |
| `request.close_after_duration` | body | `number` | no | Duration enum from 0 to 17. |
| `request.passphrase` | body | `string` | no | Optional passphrase required to view the request. |
| `request.name` | body | `string` | no | Optional dashboard name for the request. |
| `request.note` | body | `string` | no | Internal note only visible to the creator. |
| `request.retrieval_step` | body | `boolean` | no | Require an extra retrieval step. |
| `request.include_requestor` | body | `boolean` | no | Include requestor information in the request. |
| `request.response_file_attachments` | body | `boolean` | no | Allow responders to attach files. |
| `account_id` | body | `number` | no | Optional account ID for multi-account users. |
