# LeadTable: Search leads by email



```
GET https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/search-leads-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadTable `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/search-leads-by-email?connectionId=$CONNECTION_ID&limit=25&offset=0&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/search-leads-by-email?${params}`, {
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
| `email` | string | yes | Lead email address to search for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "leads": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `leads` | array<object> | Matching leads. |
| `pagination` | object | Pagination details. |

## Native endpoint

Through the native LeadTable API, this operation is `GET /searchLeadByMail/{email}` (base URL `https://api.lead-table.com/api/v3/external`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-leads-by-email.md) for the provider-specific parameters and requirements.

