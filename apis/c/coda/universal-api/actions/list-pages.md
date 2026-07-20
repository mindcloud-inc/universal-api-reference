# Coda: List Pages

Retrieves pages from a Coda doc.

```
GET https://connect.mindcloud.co/v1/universal/coda/latest/actions/list-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coda `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coda/latest/actions/list-pages?connectionId=$CONNECTION_ID&limit=25&offset=0&docId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "docId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coda/latest/actions/list-pages?${params}`, {
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
| `docId` | list | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authors": {
        "context": "string",
        "email": "ava@example.com",
        "name": "Ava Chen",
        "type": "string"
      },
      "browserLink": "https://example.com",
      "contentType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {
        "context": "string",
        "email": "ava@example.com",
        "name": "Ava Chen",
        "type": "string"
      },
      "href": "string",
      "id": "string",
      "isEffectivelyHidden": true,
      "isHidden": true,
      "name": "Ava Chen",
      "subtitle": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": {
        "context": "string",
        "email": "ava@example.com",
        "name": "Ava Chen",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authors.context` | string |  |
| `authors.email` | string |  |
| `authors.name` | string |  |
| `authors.type` | string |  |
| `browserLink` | string |  |
| `contentType` | string |  |
| `createdAt` | date |  |
| `createdBy.context` | string |  |
| `createdBy.email` | string |  |
| `createdBy.name` | string |  |
| `createdBy.type` | string |  |
| `href` | string |  |
| `id` | string |  |
| `isEffectivelyHidden` | boolean |  |
| `isHidden` | boolean |  |
| `name` | string |  |
| `subtitle` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `updatedBy.context` | string |  |
| `updatedBy.email` | string |  |
| `updatedBy.name` | string |  |
| `updatedBy.type` | string |  |

## Native endpoint

Through the native Coda API, this operation is `GET /docs/:docId/pages` (base URL `https://coda.io/apis/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pages.md) for the provider-specific parameters and requirements.

