# GoodDay.work: Get Document

Retrieves a single document from GoodDay.work.

```
GET https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoodDay.work `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/get-document?connectionId=$CONNECTION_ID&documentId=DOCUMENT-ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "DOCUMENT-ID"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/get-document?${params}`, {
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
| `documentId` | string | yes | GoodDay document ID. Default: `DOCUMENT-ID`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "createdByUserId": "string",
      "id": "string",
      "momentCreated": "string",
      "momentUpdated": "string",
      "name": "Ava Chen",
      "projectId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Document body content. |
| `createdByUserId` | string | User who created the document. |
| `id` | string | Document ID. |
| `momentCreated` | string | Creation timestamp. |
| `momentUpdated` | string | Last update timestamp. |
| `name` | string | Document name. |
| `projectId` | string | Associated project ID. |

## Native endpoint

Through the native GoodDay.work API, this operation is `GET /document/:documentId` (base URL `https://api.goodday.work/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

