# Fleetworthy: List Person Regulated Documents



```
GET https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/list-person-regulated-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetworthy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/list-person-regulated-documents?connectionId=$CONNECTION_ID&personId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "personId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/list-person-regulated-documents?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `personId` | string | yes | The Fleetworthy person UUID. |
| `isActive` | boolean | no | Return only active documents when enabled. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentDate": "2026-05-07T12:00:00.000Z",
      "expirationDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isActive": true,
      "personId": "string",
      "regulatedDocumentStatusId": "string",
      "regulatedDocumentTypeId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentDate` | date | Document date. |
| `expirationDate` | date | Document expiration date. |
| `id` | string | Regulated document identifier. |
| `isActive` | boolean | Whether the document is active. |
| `personId` | string | Owning Fleetworthy person identifier. |
| `regulatedDocumentStatusId` | string | Regulated document status identifier. |
| `regulatedDocumentTypeId` | string | Regulated document type identifier. |

## Native endpoint

Through the native Fleetworthy API, this operation is `GET /people-documents/regulated/{personId}` (base URL `https://apis.fleetworthy.com/compliance-api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-person-regulated-documents.md) for the provider-specific parameters and requirements.

