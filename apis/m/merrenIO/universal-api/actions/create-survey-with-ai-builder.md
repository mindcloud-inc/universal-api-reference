# MerrenIO: Create Survey With AI Builder



```
POST https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/create-survey-with-ai-builder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MerrenIO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/create-survey-with-ai-builder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/merrenIO/latest/actions/create-survey-with-ai-builder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt` | string | yes | Survey brief or prompt for the AI builder. |
| `name` | string | no | Name for the AI-built survey. |
| `category` | string | no | Optional category for the AI-built survey. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MerrenIO API returns.

## Native endpoint

Through the native MerrenIO API, this operation is `POST /generateSurvey/generateSurvey` (base URL `https://app.merren.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-survey-with-ai-builder.md) for the provider-specific parameters and requirements.

