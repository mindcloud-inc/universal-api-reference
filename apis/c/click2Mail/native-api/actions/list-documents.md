# List Documents with Click2Mail

Retrieves a list of documents from Click2Mail.

## Endpoint

- **Method:** `GET`
- **Path:** `/molpro/documents`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [List Documents](https://developers.click2mail.com/reference/getdocuments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `numberOfDocuments` | query | `number` | no | number of documents to return |
| `offset` | query | `number` | no | offset from beginning to allow you to paginate through the documents |
| `documentClass` | query | `string` | no | This allows you to filter by document class |
