# EyeLevel.ai: Get Health Status

Retrieves a service health status from EyeLevel.ai.

```
GET https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/get-health-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EyeLevel.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/get-health-status?connectionId=$CONNECTION_ID&service=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "service": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/get-health-status?${params}`, {
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
| `service` | string | yes | The service name to inspect, such as search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "health": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `health` | object | Current health for the requested service. |

## Native endpoint

Through the native EyeLevel.ai API, this operation is `GET /health/:service` (base URL `https://api.groundx.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-health-status.md) for the provider-specific parameters and requirements.

