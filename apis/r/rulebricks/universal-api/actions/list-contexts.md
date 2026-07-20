# Rulebricks: List Contexts

Retrieves contexts from Rulebricks.

```
GET https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/list-contexts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rulebricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/list-contexts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/list-contexts?${params}`, {
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
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "schema": {},
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Context description |
| `id` | string | Context ID |
| `name` | string | Context name |
| `schema` | object | Context schema object |
| `slug` | string | Context slug |

## Native endpoint

Through the native Rulebricks API, this operation is `GET /admin/contexts` (base URL `https://rulebricks.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contexts.md) for the provider-specific parameters and requirements.

