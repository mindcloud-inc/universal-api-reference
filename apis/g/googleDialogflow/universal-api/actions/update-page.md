# Google Dialogflow: Update Page

Updates an existing page in Google Dialogflow.

```
PUT https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/update-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Dialogflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/update-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "projects/my-project/locations/global/agents/agent-id/flows/flow-id/pages/page-id",
  "body": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/update-page', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "projects/my-project/locations/global/agents/agent-id/flows/flow-id/pages/page-id",
    "body": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `languageCode` | string | no | Optional BCP-47 language code for localized page fields. |
| `name` | string | yes | Required Dialogflow page resource name. Example: `projects/my-project/locations/global/agents/agent-id/flows/flow-id/pages/page-id`. |
| `body` | object | yes | Dialogflow Page fields to update. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `updateMask` | string | no | Optional field mask controlling which page fields are updated. Example: `displayName`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "displayName": "Ava Chen",
      "entryFulfillment": {},
      "eventHandlers": [
        {}
      ],
      "form": {},
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
| `entryFulfillment` | object |  |
| `eventHandlers` | array<object> |  |
| `form` | object |  |
| `name` | string |  |
| `transitionRouteGroups` | array<string> |  |
| `transitionRoutes` | array<object> |  |

## Native endpoint

Through the native Google Dialogflow API, this operation is `PATCH v3/:name` (base URL `https://dialogflow.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-page.md) for the provider-specific parameters and requirements.

