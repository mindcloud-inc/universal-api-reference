# Callingly: List Calls

Retrieves calls from Callingly.

```
GET https://connect.mindcloud.co/v1/universal/callingly/latest/actions/list-calls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Callingly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callingly/latest/actions/list-calls?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callingly/latest/actions/list-calls?${params}`, {
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
| `start` | string | no | Example: `2026-03-20`. |
| `end` | string | no | Example: `2026-03-21`. |
| `teamId` | number | no | Example: `19230`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "direction": "string",
      "error_message": "string",
      "id": 1,
      "phone_number_formatted": "string",
      "source": "string",
      "started_at": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `direction` | string |  |
| `error_message` | string |  |
| `id` | number |  |
| `phone_number_formatted` | string |  |
| `source` | string |  |
| `started_at` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Callingly API, this operation is `GET /v1/calls` (base URL `https://api.callingly.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-calls.md) for the provider-specific parameters and requirements.

