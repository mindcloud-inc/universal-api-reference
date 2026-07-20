# Gorgias: Retrieve Rule

Retrieves a rule from Gorgias.

```
GET https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gorgias `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-rule?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-rule?${params}`, {
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
| `id` | string | yes | Rule ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "code_ast": {},
      "created_datetime": "string",
      "deactivated_datetime": "string",
      "description": "string",
      "event_types": [
        "string"
      ],
      "id": 1,
      "name": "Ava Chen",
      "priority": 1,
      "settings": {},
      "type": "string",
      "updated_datetime": "string",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `code_ast` | object |  |
| `created_datetime` | string |  |
| `deactivated_datetime` | string |  |
| `description` | string |  |
| `event_types` | array<string> |  |
| `id` | number |  |
| `name` | string |  |
| `priority` | number |  |
| `settings` | object |  |
| `type` | string |  |
| `updated_datetime` | string |  |
| `uri` | string |  |

## Native endpoint

Through the native Gorgias API, this operation is `GET /rules/:id` (base URL `https://{{credentials.subdomain}}.gorgias.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-rule.md) for the provider-specific parameters and requirements.

