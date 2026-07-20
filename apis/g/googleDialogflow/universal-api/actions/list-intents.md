# Google Dialogflow: List Intents

Retrieves intents from Google Dialogflow.

```
GET https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/list-intents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Dialogflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/list-intents?connectionId=$CONNECTION_ID&limit=25&offset=0&parent=projects%2Fmy-project%2Flocations%2Fglobal%2Fagents%2Fagent-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "parent": "projects/my-project/locations/global/agents/agent-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/list-intents?${params}`, {
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
| `intentView` | string | no | Optional intent view controlling how much intent data is returned. |
| `parent` | string | yes | Required parent agent resource name. Example: `projects/my-project/locations/global/agents/agent-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "intents": [
        {}
      ],
      "nextPageToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `intents` | array<object> |  |
| `nextPageToken` | string |  |

## Native endpoint

Through the native Google Dialogflow API, this operation is `GET v3/:parent/intents` (base URL `https://dialogflow.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-intents.md) for the provider-specific parameters and requirements.

