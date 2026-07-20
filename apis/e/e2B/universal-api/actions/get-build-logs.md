# E2B: Get Build Logs

Retrieves logs for a template build from E2B.

```
GET https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-build-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a E2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-build-logs?connectionId=$CONNECTION_ID&buildId=string&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "buildId": "string",
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-build-logs?${params}`, {
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
| `buildId` | string | yes | Identifier of the template build. |
| `templateId` | string | yes | Identifier of the template. |

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
| `logs` | array<object> | Template build logs. |

## Native endpoint

Through the native E2B API, this operation is `GET /templates/{templateID}/builds/{buildID}/logs` (base URL `https://api.e2b.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-build-logs.md) for the provider-specific parameters and requirements.

