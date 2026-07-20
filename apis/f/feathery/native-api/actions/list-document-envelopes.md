# List Document Envelopes with Feathery

## Endpoint

- **Method:** `GET`
- **Path:** `/api/document/envelope/`
- **Base URL:** `https://api.feathery.io`
- **Official documentation:** [List Document Envelopes](https://api-docs.feathery.io/#list-document-envelopes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | If type is `document`, this is the document ID. If type is `user`, this is the user ID. |
| `type` | query | `string` | yes | Either `document` or `user`, specifying how to look up envelopes of interest. Accepted values: `0`, `1`. |
