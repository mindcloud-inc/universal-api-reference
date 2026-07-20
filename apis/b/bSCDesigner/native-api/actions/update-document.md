# Update Document with BSC Designer

## Endpoint

- **Method:** `PUT`
- **Path:** `/rest/api/documents/list/:id`
- **Base URL:** `https://www.webbsc.com`
- **Official documentation:** [Update Document](https://www.webbsc.com/swagger-ui.html#/rest-document-list-controller/updateDocumentUsingPUT)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Document id to update. |
| `name` | body | `string` | yes | Updated document name. |
| `alias` | body | `string` | no | Updated document alias. |
| `description` | body | `string` | no | Updated document description. |
| `sharedForPublic` | body | `boolean` | no | Whether the document is shared publicly. |
| `sharedForRegRW` | body | `boolean` | no | Whether the document is shared with registered users as read/write. |
