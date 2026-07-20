# EasyBroker: Update Agency Integration

Updates an agency integration status in EasyBroker.

```
PUT https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/update-agency-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyBroker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/update-agency-integration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agencyId": "string",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/update-agency-integration', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agencyId": "string",
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agencyId` | string | yes | The EasyBroker agency ID. |
| `status` | string | yes | Accepted values: paused and connected. |
| `statusReason` | string | no | Required only when status is paused. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EasyBroker API returns.

## Native endpoint

Through the native EasyBroker API, this operation is `PATCH /integration_partners/agencies/:agency_id/integration` (base URL `https://api.easybroker.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-agency-integration.md) for the provider-specific parameters and requirements.

