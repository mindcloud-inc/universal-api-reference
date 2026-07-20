# Voiceflow: Update Conversation Variables

Updates a user's conversation variables in Voiceflow.

```
PUT https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/update-conversation-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/update-conversation-variables" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "wizard-stage3-user-variables",
  "variables": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/update-conversation-variables', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "wizard-stage3-user-variables",
    "variables": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | ID of the user whose conversation variables should be merged. Example: `wizard-stage3-user-variables`. |
| `variables` | object | yes | Object of variable keys and values to merge into the user state. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "projectID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Returned state attributes, including merged variables. |
| `id` | string | Canonical session identifier for the conversation state record. |
| `projectID` | string | Voiceflow project identifier returned by the runtime state service. |

## Native endpoint

Through the native Voiceflow API, this operation is `PATCH /state/user/:userId/variables` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-conversation-variables.md) for the provider-specific parameters and requirements.

