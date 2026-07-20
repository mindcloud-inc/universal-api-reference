# Google Dialogflow: Create Flow

Creates a new flow in Google Dialogflow.

```
POST https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/create-flow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Dialogflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/create-flow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parent": "projects/my-project/locations/global/agents/agent-id",
  "body": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/create-flow', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "parent": "projects/my-project/locations/global/agents/agent-id",
    "body": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `languageCode` | string | no | Optional BCP-47 language code for localized flow fields. |
| `parent` | string | yes | Required parent agent resource name for the new flow. Example: `projects/my-project/locations/global/agents/agent-id`. |
| `body` | object | yes | Dialogflow Flow request body. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "displayName": "Ava Chen",
      "eventHandlers": [
        {}
      ],
      "locked": true,
      "name": "Ava Chen",
      "transitionRouteGroups": [
        "string"
      ],
      "transitionRoutes": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `displayName` | string |  |
| `eventHandlers` | array<object> |  |
| `locked` | boolean |  |
| `name` | string |  |
| `transitionRouteGroups` | array<string> |  |
| `transitionRoutes` | array<object> |  |

## Native endpoint

Through the native Google Dialogflow API, this operation is `POST v3/:parent/flows` (base URL `https://dialogflow.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-flow.md) for the provider-specific parameters and requirements.

