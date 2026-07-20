# Gorgias: Retrieve Widget

Retrieves a widget from Gorgias.

```
GET https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-widget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gorgias `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-widget?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-widget?${params}`, {
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
| `id` | string | yes | Widget ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "context": "string",
      "created_datetime": "string",
      "deactivated_datetime": "string",
      "id": 1,
      "integration_id": 1,
      "order": 1,
      "template": {},
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
| `context` | string |  |
| `created_datetime` | string |  |
| `deactivated_datetime` | string |  |
| `id` | number |  |
| `integration_id` | number |  |
| `order` | number |  |
| `template` | object |  |
| `type` | string |  |
| `updated_datetime` | string |  |
| `uri` | string |  |

## Native endpoint

Through the native Gorgias API, this operation is `GET /widgets/:id` (base URL `https://{{credentials.subdomain}}.gorgias.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-widget.md) for the provider-specific parameters and requirements.

