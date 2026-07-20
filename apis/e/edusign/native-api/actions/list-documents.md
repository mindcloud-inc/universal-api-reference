# List Documents with Edusign

Retrieves documents from Edusign.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/documents`
- **Base URL:** `https://ext.edusign.fr`
- **Official documentation:** [List Documents](https://developers.edusign.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `getHTML` | query | `string` | no | Retrieve or not the HTML version of the document.  <strong style="color:gold">WARNING</strong> : The weight of the HTML template can have an impact on the payload size and request speed, depending on the quantity of documents to retrieve. |
| `offset` | query | `string` | no | Query param for pagination, starts at page "0" and displays "limit" documents per page, with a maximum of 500. |
| `limit` | query | `string` | no | Query param for pagination, maximum of 500 documents per page. |
| `recipientId` | query | `string` | no | Retrieve documents based on a recipient resource ID :  - Student ID - Professor ID - External ID - Admin ID (a user with the 'admin' rights in Edusign) |
| `state` | query | `string` | no | Retrieve documents based on its signature state :  - "completed" : All recipients have signed the document - "pending" : At least one signature is still pending - "expired" : The signature link is no longer available - "refused" : The recipient(s) have refused to sign |
| `createdAfter` | query | `string` | no | Retrieve documents created after the provided date (format YYYY-MM-DDThh:mm:ss, ISO 8601) |
| `createdBefore` | query | `string` | no | Retrieve documents created before the provided date (format YYYY-MM-DDThh:mm:ss, ISO 8601) |
