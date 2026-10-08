# Fleetworthy: Search Regulated Documents



```
GET https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/search-regulated-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetworthy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/search-regulated-documents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetworthy/latest/actions/search-regulated-documents?${params}`, {
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
| `searchText` | string | no | Text used to search regulated documents. |
| `clientId` | string | no | The Fleetworthy client UUID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `advancedFilter` | object | no | Optional regulated-document filter object containing document type, status, person, date, activity, archive, Canadian, or category filters. |

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

Through the native Fleetworthy API, this operation is `POST /people-bulk/regulated-documents/search` (base URL `https://apis.fleetworthy.com/compliance-api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-regulated-documents.md) for the provider-specific parameters and requirements.

