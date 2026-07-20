# Gorgias: Retrieve Event

Retrieves an event from Gorgias.

```
GET https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gorgias `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-event?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-event?${params}`, {
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
| `id` | string | yes | Event ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "context": "string",
      "created_datetime": "string",
      "data": {},
      "id": 1,
      "object_id": 1,
      "object_type": "string",
      "type": "string",
      "uri": "string",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `context` | string |  |
| `created_datetime` | string |  |
| `data` | object |  |
| `id` | number |  |
| `object_id` | number |  |
| `object_type` | string |  |
| `type` | string |  |
| `uri` | string |  |
| `user_id` | number |  |

## Native endpoint

Through the native Gorgias API, this operation is `GET /events/:id` (base URL `https://{{credentials.subdomain}}.gorgias.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-event.md) for the provider-specific parameters and requirements.

