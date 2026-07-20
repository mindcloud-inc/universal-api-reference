# Parsio: List Documents



```
GET https://connect.mindcloud.co/v1/universal/parsio/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parsio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parsio/latest/actions/list-documents?connectionId=$CONNECTION_ID&mailboxId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mailboxId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parsio/latest/actions/list-documents?${params}`, {
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
| `mailboxId` | string | yes | Parsio mailbox ID. |
| `page` | number | no | Page number. |
| `from` | date | no | Start date in YYYY-MM-DD format. |
| `to` | date | no | End date in YYYY-MM-DD format. |
| `q` | string | no | Search query. |
| `status` | list<string> | no | Document status filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "docs": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "emailMeta": {
            "subject": "ava@example.com"
          },
          "mailboxId": "string",
          "name": "Ava Chen",
          "receivedAt": "2026-05-07T12:00:00.000Z",
          "status": "string",
          "type": "string"
        }
      ],
      "hasNextPage": true,
      "hasPrevPage": true,
      "limit": 1,
      "page": 1,
      "pagingCounter": 1,
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
| `docs` | array<object> | Document records. |
| `docs[].createdAt` | date | Document creation timestamp. |
| `docs[].emailMeta` | object | Email metadata. |
| `docs[].emailMeta.subject` | string | Email subject. |
| `docs[].mailboxId` | string | Mailbox ID. |
| `docs[].name` | string | Document name. |
| `docs[].receivedAt` | date | Document receipt timestamp. |
| `docs[].status` | string | Document status. |
| `docs[].type` | string | Document type. |
| `hasNextPage` | boolean | Whether a next page exists. |
| `hasPrevPage` | boolean | Whether a previous page exists. |
| `limit` | number | Page size. |
| `page` | number | Current page number. |
| `pagingCounter` | number | Paging counter. |
| `totalDocs` | number | Total document count. |
| `totalPages` | number | Total page count. |

## Native endpoint

Through the native Parsio API, this operation is `GET /mailboxes/:mailbox_id/docs` (base URL `https://api.parsio.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

