# Create Person Regulated Document with Fleetworthy

## Endpoint

- **Method:** `POST`
- **Path:** `/people-documents/regulated`
- **Base URL:** `https://apis.fleetworthy.com/compliance-api/v1`
- **Official documentation:** [Create Person Regulated Document](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=post-people-documents-regulated)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `RegulatedDocumentTypeId` | body | `string` | yes | The regulated document type ID from People Client Metadata. |
| `DocumentDate` | body | `date` | yes | The date shown on the document. |
| `RequestedDate` | body | `date` | no | The date the document was requested. |
| `ExpirationDate` | body | `date` | no | The document expiration date when applicable. |
| `RegulatedDocumentStatusId` | body | `string` | yes | The status ID from Person Metadata. |
| `PersonId` | body | `string` | yes | The Fleetworthy person UUID. |
| `IsActive` | body | `boolean` | yes | Whether the regulated document is active. |
| `LocationId` | body | `string` | yes | The Fleetworthy location UUID. |
| `ObjectId` | body | `string` | yes | The object identifier required by Fleetworthy's multipart contract. |
| `ParentObjectId` | body | `string` | yes | The parent person identifier required by Fleetworthy's multipart contract. |
| `ObjectDisplayName` | body | `string` | yes | The display name for the uploaded report. |
| `SetAsPrimary` | body | `boolean` | yes | Whether the uploaded file is the primary file for the document. |
| `UserId` | body | `string` | no | Optional Fleetworthy user UUID associated with the upload. |
| `MetaData` | body | `string` | yes | Fleetworthy metadata string for the uploaded file. |
| `file` | body | `file` | yes | The report file to upload. |
