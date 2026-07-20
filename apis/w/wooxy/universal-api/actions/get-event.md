# Wooxy: Get Event

Retrieves an event from your Wooxy account.

```
GET https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/get-event?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/get-event?${params}`, {
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
| `id` | string | no | The Wooxy event ID. Use this or Event Name. Example: `69d68d2a363c31463001917d`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | The Wooxy event name. Use this or Event ID. Example: `Stage3Purchase20260408`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "cost": {},
        "createdAt": "string",
        "description": "string",
        "id": "string",
        "isConversion": true,
        "name": "Ava Chen",
        "updatedAt": "string"
      },
      "errors": [
        "string"
      ],
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data.cost` | object |  |
| `data.createdAt` | string |  |
| `data.description` | string |  |
| `data.id` | string |  |
| `data.isConversion` | boolean |  |
| `data.name` | string |  |
| `data.updatedAt` | string |  |
| `errors` | array<string> |  |
| `result` | boolean |  |

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/custom-event/get` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

