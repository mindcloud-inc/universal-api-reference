# Port API AI: Update Action Automation

Updates an action automation in Port.

```
PUT https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-action-automation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-action-automation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actionIdentifier": "string",
  "identifier": "string",
  "invocationMethod": {},
  "trigger": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-action-automation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actionIdentifier": "string",
    "identifier": "string",
    "invocationMethod": {},
    "trigger": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `actionIdentifier` | string | yes | The action identifier. |
| `identifier` | string | yes | The action identifier. |
| `invocationMethod` | object | yes | The invocation method object. |
| `trigger` | object | yes | The action trigger object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": {},
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | object |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Port API AI API, this operation is `PUT /actions/:action_identifier` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-action-automation.md) for the provider-specific parameters and requirements.

