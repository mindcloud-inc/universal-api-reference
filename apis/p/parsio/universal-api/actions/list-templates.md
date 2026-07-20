# Parsio: List Templates



```
GET https://connect.mindcloud.co/v1/universal/parsio/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parsio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parsio/latest/actions/list-templates?connectionId=$CONNECTION_ID&mailboxId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mailboxId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parsio/latest/actions/list-templates?${params}`, {
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
| `docs` | array<object> | Template records. |
| `hasNextPage` | boolean | Whether a next page exists. |
| `hasPrevPage` | boolean | Whether a previous page exists. |
| `limit` | number | Page size. |
| `page` | number | Current page number. |
| `pagingCounter` | number | Paging counter. |
| `totalDocs` | number | Total template count. |
| `totalPages` | number | Total page count. |

## Native endpoint

Through the native Parsio API, this operation is `GET /mailboxes/:mb_id/templates` (base URL `https://api.parsio.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

