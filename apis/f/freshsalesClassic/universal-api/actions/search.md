# Freshsales Classic: Search

Finds records in Freshsales Classic by query.

```
GET https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshsales Classic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/search?connectionId=$CONNECTION_ID&include=string&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "include": "string",
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/search?${params}`, {
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
| `include` | string | yes | Entity types to include in the search, for example contact, sales_account, deal, or user. |
| `page` | number | no | Page number to return. |
| `perPage` | number | no | Maximum number of results to return per page. |
| `q` | string | yes | Search text to look up in Freshsales Classic. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "id": "string",
      "isActive": true,
      "name": "Ava Chen",
      "type": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Search result email when available. |
| `id` | string | Search result ID. |
| `isActive` | boolean | Whether the matched user is active. |
| `name` | string | Search result name. |
| `type` | string | Freshsales entity type for the search result. |
| `uuid` | string | Freshsales UUID for the result when available. |

## Native endpoint

Through the native Freshsales Classic API, this operation is `GET /search` (base URL `https://{{credentials.bundleAlias}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search.md) for the provider-specific parameters and requirements.

