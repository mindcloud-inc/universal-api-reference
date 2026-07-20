# Parsio: Get Parsed Data



```
GET https://connect.mindcloud.co/v1/universal/parsio/latest/actions/get-parsed-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parsio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parsio/latest/actions/get-parsed-data?connectionId=$CONNECTION_ID&mailboxId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mailboxId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parsio/latest/actions/get-parsed-data?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "docIds": [
        "string"
      ],
      "docs": [
        {}
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
| `docIds` | array<string> | Parsed document IDs. |
| `docs` | array<object> | Parsed document rows. |
| `hasNextPage` | boolean | Whether a next page exists. |
| `hasPrevPage` | boolean | Whether a previous page exists. |
| `limit` | number | Page size. |
| `page` | number | Current page number. |
| `pagingCounter` | number | Paging counter. |
| `totalDocs` | number | Total parsed document count. |
| `totalPages` | number | Total page count. |

## Native endpoint

Through the native Parsio API, this operation is `GET /mailboxes/:mailbox_id/parsed` (base URL `https://api.parsio.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-parsed-data.md) for the provider-specific parameters and requirements.

