# List Job Documents with Click2Mail

Retrieves a list of job documents from Click2Mail.

## Endpoint

- **Method:** `GET`
- **Path:** `/molpro/documents/jobDocuments`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [List Job Documents](https://developers.click2mail.com/reference/getjobdocuments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | query | `string` | yes | The document id |
| `offset` | query | `number` | no | offset from beginning to allow you to paginate through the documents |
| `numberOfDocuments` | query | `number` | no | number of documents to return |
