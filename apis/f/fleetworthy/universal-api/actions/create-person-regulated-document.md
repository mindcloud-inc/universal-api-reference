# Fleetworthy: Create Person Regulated Document



```
POST https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/create-person-regulated-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetworthy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/create-person-regulated-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "regulatedDocumentTypeId": "string",
  "documentDate": "2026-05-07T12:00:00.000Z",
  "regulatedDocumentStatusId": "string",
  "personId": "string",
  "isActive": "true",
  "locationId": "string",
  "objectId": "string",
  "parentObjectId": "string",
  "objectDisplayName": "Ava Chen",
  "setAsPrimary": "true",
  "metaData": "string",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/create-person-regulated-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "regulatedDocumentTypeId": "string",
    "documentDate": "2026-05-07T12:00:00.000Z",
    "regulatedDocumentStatusId": "string",
    "personId": "string",
    "isActive": "true",
    "locationId": "string",
    "objectId": "string",
    "parentObjectId": "string",
    "objectDisplayName": "Ava Chen",
    "setAsPrimary": "true",
    "metaData": "string",
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `regulatedDocumentTypeId` | string | yes | The regulated document type ID from People Client Metadata. |
| `documentDate` | date | yes | The date shown on the document. |
| `requestedDate` | date | no | The date the document was requested. |
| `expirationDate` | date | no | The document expiration date when applicable. |
| `regulatedDocumentStatusId` | string | yes | The status ID from Person Metadata. |
| `personId` | string | yes | The Fleetworthy person UUID. |
| `isActive` | boolean | yes | Whether the regulated document is active. Default: `true`. |
| `locationId` | string | yes | The Fleetworthy location UUID. |
| `objectId` | string | yes | The object identifier required by Fleetworthy's multipart contract. |
| `parentObjectId` | string | yes | The parent person identifier required by Fleetworthy's multipart contract. |
| `objectDisplayName` | string | yes | The display name for the uploaded report. |
| `setAsPrimary` | boolean | yes | Whether the uploaded file is the primary file for the document. Default: `true`. |
| `file` | file | yes | The report file to upload. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | no | Optional Fleetworthy user UUID associated with the upload. |
| `metaData` | string | yes | Fleetworthy metadata string for the uploaded file. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fleetworthy API returns.

## Native endpoint

Through the native Fleetworthy API, this operation is `POST /people-documents/regulated` (base URL `https://apis.fleetworthy.com/compliance-api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-person-regulated-document.md) for the provider-specific parameters and requirements.

