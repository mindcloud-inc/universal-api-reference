# Maildrip: Get opt-in pages



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-opt-in-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-opt-in-pages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-opt-in-pages?${params}`, {
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
| `search` | string | no | Search term to filter opt-in pages by title |
| `limit` | string | no | Number of items per page or "all" to retrieve all pages |
| `page` | number | no | Page number for pagination |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "optInPages": [
        {}
      ],
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of items |
| `optInPages` | array<object> | Array of opt-in pages |
| `totalPages` | number | Total number of pages |

## Native endpoint

Through the native Maildrip API, this operation is `GET /api/v1/opt-in-pages` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-opt-in-pages.md) for the provider-specific parameters and requirements.

