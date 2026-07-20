# Enrich.so: List Saved Searches

Retrieves saved searches from Enrich.so.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/list-saved-searches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/list-saved-searches?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/list-saved-searches?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "filters": {},
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Saved search creation timestamp. |
| `filters` | object | Saved filter configuration. |
| `id` | string | Saved search identifier. |
| `name` | string | Saved search name. |
| `updatedAt` | date | Saved search update timestamp. |

## Native endpoint

Through the native Enrich.so API, this operation is `GET /lead-finder/saved` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-saved-searches.md) for the provider-specific parameters and requirements.

