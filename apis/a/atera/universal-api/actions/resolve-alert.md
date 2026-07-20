# Atera: Resolve alert

Updates an existing alert in Atera as resolved.

```
PUT https://connect.mindcloud.co/v1/universal/atera/latest/actions/resolve-alert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/atera/latest/actions/resolve-alert" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "alertId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/atera/latest/actions/resolve-alert', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "alertId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `alertId` | number | yes | System alert ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alertId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alertId` | number | Resolved alert ID inferred from the request when Atera returns no response body. |

## Native endpoint

Through the native Atera API, this operation is `PUT /api/v3/alerts/:alertId` (base URL `https://app.atera.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resolve-alert.md) for the provider-specific parameters and requirements.

