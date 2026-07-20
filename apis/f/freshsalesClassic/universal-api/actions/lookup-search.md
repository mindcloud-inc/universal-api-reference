# Freshsales Classic: Lookup Search

Finds lookup records in Freshsales Classic by query.

```
GET https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/lookup-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshsales Classic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/lookup-search?connectionId=$CONNECTION_ID&entities=string&f=string&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entities": "string",
  "f": "string",
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/lookup-search?${params}`, {
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
| `entities` | string | yes | Entity type to search, for example contact. |
| `f` | string | yes | Field to match during lookup search, for example email. |
| `q` | string | yes | Lookup text to search for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Lookup result email when present. |
| `id` | string | Lookup result ID. |
| `name` | string | Lookup result name. |
| `type` | string | Lookup result entity type. |

## Native endpoint

Through the native Freshsales Classic API, this operation is `GET /lookup` (base URL `https://{{credentials.bundleAlias}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-search.md) for the provider-specific parameters and requirements.

