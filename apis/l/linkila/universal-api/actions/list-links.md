# Linkila: List Links

Retrieves saved links from Linkila.

```
GET https://connect.mindcloud.co/v1/universal/linkila/latest/actions/list-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkila `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkila/latest/actions/list-links?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkila/latest/actions/list-links?${params}`, {
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
| `data` | array<object> | Array of Link records. Runtime verified with id, title, defaultDestinationURL, shortUrls, tags, and filterDestinations. |
| `pageInfo` | object | Pagination metadata: hasNextPage, hasPreviousPage, nextCurosr, prevCursor. |

## Native endpoint

Through the native Linkila API, this operation is `GET /links` (base URL `https://app.linkila.com/integrations/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-links.md) for the provider-specific parameters and requirements.

