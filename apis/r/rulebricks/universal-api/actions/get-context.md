# Rulebricks: Get Context

Retrieves a context from Rulebricks.

```
GET https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/get-context
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rulebricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/get-context?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/get-context?${params}`, {
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
| `id` | string | yes | ID of the context to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "relationships": {},
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
| `relationships` | object | Context relationship object |
| `schema` | object | Context schema object |
| `slug` | string | Context slug |

## Native endpoint

Through the native Rulebricks API, this operation is `GET /admin/contexts/:id` (base URL `https://rulebricks.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-context.md) for the provider-specific parameters and requirements.

