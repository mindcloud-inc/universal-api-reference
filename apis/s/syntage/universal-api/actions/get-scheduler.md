# Syntage: Get Scheduler

Retrieves a scheduler from Syntage.

```
GET https://connect.mindcloud.co/v1/universal/syntage/latest/actions/get-scheduler
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syntage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syntage/latest/actions/get-scheduler?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syntage/latest/actions/get-scheduler?${params}`, {
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
| `id` | string | yes | The scheduler identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@id": "string",
      "@type": "string",
      "createdAt": "string",
      "id": "string",
      "isEnabled": true,
      "name": "Ava Chen",
      "rules": {},
      "tags": [
        {}
      ],
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@id` | string |  |
| `@type` | string |  |
| `createdAt` | string |  |
| `id` | string |  |
| `isEnabled` | boolean |  |
| `name` | string |  |
| `rules` | object |  |
| `tags` | array<object> |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Syntage API, this operation is `GET /schedulers/:id` (base URL `https://api.sandbox.syntage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-scheduler.md) for the provider-specific parameters and requirements.

