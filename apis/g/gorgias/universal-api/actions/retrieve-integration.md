# Gorgias: Retrieve Integration

Retrieves an integration from Gorgias.

```
GET https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gorgias `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-integration?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-integration?${params}`, {
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
| `id` | string | yes | Integration ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "application_id": 1,
      "business_hours_id": 1,
      "created_datetime": "string",
      "deactivated_datetime": "string",
      "decoration": {},
      "description": "string",
      "http": {},
      "id": 1,
      "locked_datetime": "string",
      "managed": true,
      "meta": {},
      "name": "Ava Chen",
      "type": "string",
      "updated_datetime": "string",
      "uri": "string",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `application_id` | number |  |
| `business_hours_id` | number |  |
| `created_datetime` | string |  |
| `deactivated_datetime` | string |  |
| `decoration` | object |  |
| `description` | string |  |
| `http` | object |  |
| `id` | number |  |
| `locked_datetime` | string |  |
| `managed` | boolean |  |
| `meta` | object |  |
| `name` | string |  |
| `type` | string |  |
| `updated_datetime` | string |  |
| `uri` | string |  |
| `user` | object |  |

## Native endpoint

Through the native Gorgias API, this operation is `GET /integrations/:id` (base URL `https://{{credentials.subdomain}}.gorgias.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-integration.md) for the provider-specific parameters and requirements.

