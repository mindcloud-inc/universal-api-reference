# Google Dialogflow: Get Agent Validation Result

Retrieves an agent validation result from Google Dialogflow.

```
GET https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/get-agent-validation-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Dialogflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/get-agent-validation-result?connectionId=$CONNECTION_ID&name=projects%2Fmy-project%2Flocations%2Fglobal%2Fagents%2Fagent-id%2FvalidationResult" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "projects/my-project/locations/global/agents/agent-id/validationResult"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleDialogflow/latest/actions/get-agent-validation-result?${params}`, {
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
| `name` | string | yes | Required agent validation result resource name. Example: `projects/my-project/locations/global/agents/agent-id/validationResult`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "flowValidationResults": [
        {}
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `flowValidationResults` | array<object> |  |
| `name` | string |  |

## Native endpoint

Through the native Google Dialogflow API, this operation is `GET v3/:name` (base URL `https://dialogflow.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-validation-result.md) for the provider-specific parameters and requirements.

