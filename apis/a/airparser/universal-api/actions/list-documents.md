# Airparser: List Documents

Retrieves documents from an Airparser inbox.

```
GET https://connect.mindcloud.co/v1/universal/airparser/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airparser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airparser/latest/actions/list-documents?connectionId=$CONNECTION_ID&inboxId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inboxId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airparser/latest/actions/list-documents?${params}`, {
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
| `inboxId` | string | yes | The Airparser inbox ID. |
| `page` | number | no | Page number for paginated document results. |
| `from` | date | no | Start date in YYYY-MM-DD format. |
| `to` | date | no | End date in YYYY-MM-DD format. |
| `q` | string | no | Text search query. |
| `statuses` | list<string> | no | Document statuses to include. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "docs": [
        {}
      ],
      "hasNextPage": true,
      "hasPrevPage": true,
      "limit": 1,
      "nextPage": 1,
      "page": 1,
      "pagingCounter": 1,
      "prevPage": 1,
      "totalDocs": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `docs` | array<object> |  |
| `hasNextPage` | boolean |  |
| `hasPrevPage` | boolean |  |
| `limit` | number |  |
| `nextPage` | number |  |
| `page` | number |  |
| `pagingCounter` | number |  |
| `prevPage` | number |  |
| `totalDocs` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Airparser API, this operation is `GET /inboxes/:inbox_id/docs` (base URL `https://api.airparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

