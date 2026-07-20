# Mark Sending Request Uploaded with RightSignature

Marks a RightSignature sending request upload as complete.

## Endpoint

- **Method:** `POST`
- **Path:** `/sending_requests/:id/uploaded`
- **Base URL:** `https://api.rightsignature.com/public/v2`
- **Official documentation:** [Mark Sending Request Uploaded](https://api.rightsignature.com/documentation/resources/v2/sending_requests/uploaded.en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Sending Request ID |
| `prepare_document` | body | `boolean` | no | Whether the document should be sent or an url to be returned for preparing the document |
