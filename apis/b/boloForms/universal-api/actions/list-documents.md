# BoloForms: List Documents

Retrieves documents from BoloForms.

```
GET https://connect.mindcloud.co/v1/universal/boloForms/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoloForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boloForms/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boloForms/latest/actions/list-documents?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "authorEmail": "ava@example.com",
      "createdAt": "string",
      "createdBy": {},
      "documentId": "string",
      "documentName": "Ava Chen",
      "documentUrl": "https://example.com",
      "history": [
        {}
      ],
      "Id": "string",
      "isAllSigned": true,
      "isArchived": true,
      "isSigningOrderData": true,
      "metafields": {},
      "pagesCount": 1,
      "respondentsOfDoc": [
        {}
      ],
      "roles": [
        {}
      ],
      "schemaFieldsCount": 1,
      "sentViaSMS": true,
      "settings": {},
      "signType": "string",
      "status": "string",
      "totalRespondants": 1,
      "totalSignedRespondants": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorEmail` | string |  |
| `createdAt` | string |  |
| `createdBy` | object |  |
| `documentId` | string |  |
| `documentName` | string |  |
| `documentUrl` | string |  |
| `history` | array<object> |  |
| `Id` | string |  |
| `isAllSigned` | boolean |  |
| `isArchived` | boolean |  |
| `isSigningOrderData` | boolean |  |
| `metafields` | object |  |
| `pagesCount` | number |  |
| `respondentsOfDoc` | array<object> |  |
| `roles` | array<object> |  |
| `schemaFieldsCount` | number |  |
| `sentViaSMS` | boolean |  |
| `settings` | object |  |
| `signType` | string |  |
| `status` | string |  |
| `totalRespondants` | number |  |
| `totalSignedRespondants` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native BoloForms API, this operation is `GET /get-documents` (base URL `https://sapi.boloforms.com/signature`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

