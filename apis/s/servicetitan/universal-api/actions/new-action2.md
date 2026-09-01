# ServiceTitan: Update Payment Custom Fields



```
PUT https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/new-action2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/new-action2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "paymentId": "123456",
  "customFieldName": "VistaID",
  "customFieldValue": "1:2026-08-01T00:00:00:4257:1382"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/new-action2', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "paymentId": "123456",
    "customFieldName": "VistaID",
    "customFieldValue": "1:2026-08-01T00:00:00:4257:1382"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `paymentId` | string | yes | Example: `123456`. |
| `customFieldName` | string | yes | Exact name of the ServiceTitan Payment custom field. For the United Mechanical production tenant, use Vista ID. Default: `Vista ID`. Example: `VistaID`. |
| `customFieldValue` | string | yes | Example: `1:2026-08-01T00:00:00:4257:1382`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ServiceTitan API returns.

## Native endpoint

Through the native ServiceTitan API, this operation is `PATCH accounting/v2/tenant/{{credentials.tenant}}/payments/custom-fields` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/new-action2.md) for the provider-specific parameters and requirements.

