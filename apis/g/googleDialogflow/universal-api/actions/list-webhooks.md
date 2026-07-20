# Google Dialogflow: List Webhooks

Retrieves webhooks from Google Dialogflow.

```
GET https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Dialogflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&limit=25&offset=0&parent=projects%2Fmy-project%2Flocations%2Fglobal%2Fagents%2Fagent-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "parent": "projects/my-project/locations/global/agents/agent-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/list-webhooks?${params}`, {
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
| `parent` | string | yes | Required parent agent resource name. Example: `projects/my-project/locations/global/agents/agent-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPageToken": "string",
      "webhooks": [
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
| `nextPageToken` | string |  |
| `webhooks` | array<object> |  |

## Native endpoint

Through the native Google Dialogflow API, this operation is `GET v3/:parent/webhooks` (base URL `https://dialogflow.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

