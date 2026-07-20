# Google Dialogflow: Update Agent

Updates an existing agent in Google Dialogflow.

```
PUT https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/update-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Dialogflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/update-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "projects/my-project/locations/global/agents/agent-id",
  "body": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/update-agent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "projects/my-project/locations/global/agents/agent-id",
    "body": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Required Dialogflow agent resource name. Example: `projects/my-project/locations/global/agents/agent-id`. |
| `body` | object | yes | Dialogflow Agent fields to update. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `updateMask` | string | no | Optional field mask controlling which agent fields are updated. Example: `displayName,timeZone`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defaultLanguageCode": "string",
      "description": "string",
      "displayName": "Ava Chen",
      "enableSpellCorrection": true,
      "enableStackdriverLogging": true,
      "locked": true,
      "name": "Ava Chen",
      "startFlow": "string",
      "supportedLanguageCodes": [
        "string"
      ],
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultLanguageCode` | string |  |
| `description` | string |  |
| `displayName` | string |  |
| `enableSpellCorrection` | boolean |  |
| `enableStackdriverLogging` | boolean |  |
| `locked` | boolean |  |
| `name` | string |  |
| `startFlow` | string |  |
| `supportedLanguageCodes` | array<string> |  |
| `timeZone` | string |  |

## Native endpoint

Through the native Google Dialogflow API, this operation is `PATCH v3/:name` (base URL `https://dialogflow.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-agent.md) for the provider-specific parameters and requirements.

