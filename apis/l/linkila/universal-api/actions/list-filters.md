# Linkila: List Filters

Retrieves saved filters from Linkila.

```
GET https://connect.mindcloud.co/v1/universal/linkila/latest/actions/list-filters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkila `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkila/latest/actions/list-filters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkila/latest/actions/list-filters?${params}`, {
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
| `cursor` | string | no | Cursor for pagination. Use the cursor returned in pageInfo from a previous response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "pageInfo": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Array of Filter records. Runtime returned an empty 200; schema is derived from official docs. |
| `pageInfo` | object | Pagination metadata: hasNextPage, hasPreviousPage, nextCurosr, prevCursor. |

## Native endpoint

Through the native Linkila API, this operation is `GET /filters` (base URL `https://app.linkila.com/integrations/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-filters.md) for the provider-specific parameters and requirements.

