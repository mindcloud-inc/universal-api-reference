# Nyne AI: Search Companies

Finds companies in Nyne AI by industry or keyword.

```
GET https://connect.mindcloud.co/v1/universal/nyneAI/latest/actions/search-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nyne AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nyneAI/latest/actions/search-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nyneAI/latest/actions/search-companies?${params}`, {
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
      "created_on": "2026-05-07T12:00:00.000Z",
      "limit": 1,
      "message": "string",
      "next_cursor": "string",
      "offset": 1,
      "request_id": "string",
      "results": [
        {}
      ],
      "status": "string",
      "success": true,
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_on` | date | Job creation timestamp. |
| `limit` | number | Requested or returned page size. |
| `message` | string | Provider status message. |
| `next_cursor` | string | Cursor for a subsequent request when provided. |
| `offset` | number | Result offset. |
| `request_id` | string | Nyne request identifier. |
| `results` | array<object> | Company search results. |
| `status` | string | Processing status. |
| `success` | boolean | Whether the search completed or was accepted. |
| `timestamp` | date | Response timestamp. |

## Native endpoint

Through the native Nyne AI API, this operation is `POST /company/search` (base URL `https://api.nyne.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-companies.md) for the provider-specific parameters and requirements.

