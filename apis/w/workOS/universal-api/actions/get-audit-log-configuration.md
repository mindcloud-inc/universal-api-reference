# WorkOS: Get Audit Log Configuration

Retrieves audit log configuration from your WorkOS environment.

```
GET https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-audit-log-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-audit-log-configuration?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-audit-log-configuration?${params}`, {
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
| `id` | string | yes | Unique identifier of the Organization. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "log_stream": {},
      "message": "string",
      "object": "string",
      "organization_id": "string",
      "retention_period_in_days": 1,
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | WorkOS response field id. |
| `log_stream` | object | The Audit Log Stream currently configured for the organization, if any. |
| `message` | string | WorkOS response field message. |
| `object` | string | WorkOS response field object. |
| `organization_id` | string | Unique identifier of the Organization. |
| `retention_period_in_days` | number | The number of days Audit Log events will be retained before being permanently deleted. |
| `state` | string | The current state of the audit log configuration for the organization. |

## Native endpoint

Through the native WorkOS API, this operation is `GET /organizations/{id}/audit_log_configuration` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-audit-log-configuration.md) for the provider-specific parameters and requirements.

