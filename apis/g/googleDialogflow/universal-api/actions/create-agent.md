# Google Dialogflow: Create Agent

Creates a new agent in Google Dialogflow.

```
POST https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/create-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Dialogflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/create-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parent": "projects/my-project/locations/global",
  "body": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/create-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "parent": "projects/my-project/locations/global",
    "body": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parent` | string | yes | Required parent location resource name for the new agent. Example: `projects/my-project/locations/global`. |
| `body` | object | yes | Dialogflow Agent request body. Example: `[object Object]`. |

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

Through the native Google Dialogflow API, this operation is `POST v3/:parent/agents` (base URL `https://dialogflow.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agent.md) for the provider-specific parameters and requirements.

