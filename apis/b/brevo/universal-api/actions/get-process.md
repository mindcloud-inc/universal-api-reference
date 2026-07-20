# Brevo: Get Process



```
GET https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-process
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-process?connectionId=$CONNECTION_ID&processId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "processId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-process?${params}`, {
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
| `processId` | number | yes | The process identifier returned by Brevo. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "export_url": "https://example.com",
      "id": 1,
      "info": {},
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `export_url` | string | The export file URL when available. |
| `id` | number | The process id. |
| `info` | object | Additional process details. |
| `name` | string | The process name. |
| `status` | string | The process status. |

## Native endpoint

Through the native Brevo API, this operation is `GET /v3/processes/:processId` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-process.md) for the provider-specific parameters and requirements.

