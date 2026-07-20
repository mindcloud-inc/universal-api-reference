# Create Document Using Base64 with Edusign

Creates a new document in Edusign from Base64.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/documents`
- **Base URL:** `https://ext.edusign.fr`
- **Official documentation:** [Create Document Using Base64](https://developers.edusign.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `directoryId` | body | `string` | no | Sélectionnez le dossier existant dans lequel vous souhaitez enregistrer les documents que vous créez |
| `trainingId` | body | `string` | no | This field is used to select the existing training in which you want to link the documents you are creating |
| `sendDocumentToSignByEmail` | body | `string` | yes | This field is used to choose if the document should be sent by email to all recipients to allow them to sign it. Default: true |
| `sendDocumentByEmailWhenCompleted` | body | `string` | yes | This field is used to choose if the document should be sent by email to all recipients once it is fully signed. Default: true |
| `redirectionLinkOnceSigned` | body | `string` | no | Redirigez l'utilisateur vers une URL spécifique une fois qu'il a signé |
| `signatureValidationMethod` | body | `string` | yes | Allowed values: "email", "sms", "none" (none make the signature validation optional). Default: "email" |
| `signWithOrder` | body | `boolean` | yes | This field allows to send the document to the recipients one after the other only when the previous recipient has signed |
| `expirationDate` | body | `string` | no | This field allows you to define a date from which it will no longer be possible to sign the document |
| `attachedDocuments[]` | body | `array<object>` | no | — |
| `sendCustomDocumentEmail` | body | `object` | no | — |
| `sendCustomDocumentEmail.subject` | body | `string` | yes | The subject of the email |
| `sendCustomDocumentEmail.body` | body | `string` | yes | The body of the email |
| `sendCustomSignatureReminderEmail` | body | `object` | no | — |
| `sendCustomSignatureReminderEmail.subject` | body | `string` | yes | The subject of the email |
| `sendCustomSignatureReminderEmail.body` | body | `string` | yes | The body of the email |
| `sendCustomSignatureReminderEmail.amount` | body | `number` | yes | The number of reminder emails you want to send |
| `sendCustomSignatureReminderEmail.interval` | body | `number` | yes | The interval in hours between each reminder email (in hours) |
| `sendCustomEmailWhenDocumentCompleted` | body | `object` | no | — |
| `sendCustomEmailWhenDocumentCompleted.subject` | body | `string` | yes | The subject of the email |
| `sendCustomEmailWhenDocumentCompleted.body` | body | `string` | yes | The body of the email |
| `admin_id` | body | `string` | yes | The ID of the admin who sends the document |
| `recipients[]` | body | `array<array>` | yes | An array containing arrays of recipients for each document to be sent <br> Each array of recipients represents a document that will be sent. All recipient arrays must be identical (same number of recipients in the same order), only the IDs must be different from one array to another <strong style="color:gold">WARNING</strong> : All recipient arrays must be identical (same number of recipients in the same order), only the IDs must be different from one array to another |
| `inputs[]` | body | `array<object>` | yes | — |
| `document` | body | `object` | yes | The document you want to send |
| `document.name` | body | `string` | yes | The name of the document |
| `document.base64` | body | `string` | yes | The base64 string of the document |
| `useNativeCoordinates` | body | `boolean` | no | This field allows you to use native coordinates for the document? If true, the coordinates will be used as is, if false, the coordinates will be scaled to the document size |
| `attachedDocuments[name]` | body | `string` | yes | Nom du document joint |
| `attachedDocuments[url]` | body | `string` | yes | URL du document joint |
