# E2B: Get Sandbox Logs V2

Retrieves logs for a sandbox from E2B.

```
GET https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-sandbox-logs-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a E2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-sandbox-logs-v2?connectionId=$CONNECTION_ID&sandboxId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sandboxId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-sandbox-logs-v2?${params}`, {
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
| `sandboxId` | string | yes | Identifier of the sandbox. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "logs": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `logs` | array<object> | Structured sandbox logs. |

## Native endpoint

Through the native E2B API, this operation is `GET /v2/sandboxes/{sandboxID}/logs` (base URL `https://api.e2b.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sandbox-logs-v2.md) for the provider-specific parameters and requirements.

