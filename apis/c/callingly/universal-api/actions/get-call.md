# Callingly: Get Call

Retrieves a call from Callingly.

```
GET https://connect.mindcloud.co/v1/universal/callingly/latest/actions/get-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Callingly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callingly/latest/actions/get-call?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callingly/latest/actions/get-call?${params}`, {
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
| `id` | number | yes | The Callingly call ID to retrieve. |

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

Through the native Callingly API, this operation is `GET /v1/calls/{{id}}` (base URL `https://api.callingly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call.md) for the provider-specific parameters and requirements.

