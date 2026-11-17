# Viewpoint Vista: Update Contract Item



```
PUT https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/update-contract-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/update-contract-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "__key": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/update-contract-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "__key": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `__key` | object | yes | Object { "JCCo": number, "Contract": string (≤ 10), "Item": string (≤ 16) }, or { "KeyID": number } of the contract item. |
| `Department` | string | no | Key to jc/departments(JCCo, Department). Optional. If omitted, existing value in Vista will remain unchanged. |
| `Description` | string | no | Optional. If omitted, existing value in Vista will remain unchanged. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "operation": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Action instance id. Pass it to Get Action Instance (action_key_value). |
| `operation` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/jc/2/data/contracts/actions/chg_line` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contract-item.md) for the provider-specific parameters and requirements.

