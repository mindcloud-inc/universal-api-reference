# Airzone Cloud: Update Installation

Updates all climate zones in an installation in Airzone Cloud.

```
PUT https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/update-installation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airzone Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/update-installation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "installationId": "string",
  "params": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/update-installation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "installationId": "string",
    "params": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `installationId` | string | yes | The Airzone installation identifier. |
| `params` | object | yes | Object of installation-wide climate changes to apply, such as `power`, `mode`, `setpoint`, or `speed`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `opts` | object | no | Optional object for extra settings, such as `units` when sending a setpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the installation update request succeeded. |

## Native endpoint

Through the native Airzone Cloud API, this operation is `PUT /installations/{installationId}` (base URL `https://m.airzonecloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-installation.md) for the provider-specific parameters and requirements.

