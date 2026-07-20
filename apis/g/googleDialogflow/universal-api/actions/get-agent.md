# Google Dialogflow: Get Agent

Retrieves an agent from Google Dialogflow.

```
GET https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/get-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Dialogflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/get-agent?connectionId=$CONNECTION_ID&name=projects%2Fmy-project%2Flocations%2Fglobal%2Fagents%2Fagent-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "projects/my-project/locations/global/agents/agent-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/get-agent?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Required Dialogflow agent resource name. Example: `projects/my-project/locations/global/agents/agent-id`. |

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

Through the native Google Dialogflow API, this operation is `GET v3/:name` (base URL `https://dialogflow.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent.md) for the provider-specific parameters and requirements.

