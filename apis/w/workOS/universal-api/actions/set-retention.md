# WorkOS: Set Retention

Sets retention in your WorkOS environment.

```
PUT https://connect.mindcloud.co/v1/universal/workOS/latest/actions/set-retention
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/set-retention" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "retention_period_in_days": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workOS/latest/actions/set-retention', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "retention_period_in_days": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique identifier of the Organization. |
| `retention_period_in_days` | number | yes | The number of days Audit Log events will be retained. Valid values are `30` and `365`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string",
      "object": "string",
      "retention_period_in_days": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | WorkOS response field id. |
| `message` | string | WorkOS response field message. |
| `object` | string | WorkOS response field object. |
| `retention_period_in_days` | number | The number of days Audit Log events will be retained before being permanently deleted. Valid values are 30 and 365. |

## Native endpoint

Through the native WorkOS API, this operation is `PUT /organizations/{id}/audit_logs_retention` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-retention.md) for the provider-specific parameters and requirements.

