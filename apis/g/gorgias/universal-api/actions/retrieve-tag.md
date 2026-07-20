# Gorgias: Retrieve Tag

Retrieves a tag from Gorgias.

```
GET https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gorgias `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-tag?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-tag?${params}`, {
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
| `id` | string | yes | Tag ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_datetime": "string",
      "decoration": {},
      "deleted_datetime": "string",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "uri": "string",
      "usage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_datetime` | string |  |
| `decoration` | object |  |
| `deleted_datetime` | string |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `uri` | string |  |
| `usage` | object |  |

## Native endpoint

Through the native Gorgias API, this operation is `GET /tags/:id` (base URL `https://{{credentials.subdomain}}.gorgias.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-tag.md) for the provider-specific parameters and requirements.

