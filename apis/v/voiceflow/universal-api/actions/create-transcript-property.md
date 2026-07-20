# Voiceflow: Create Transcript Property

Creates a new transcript property in Voiceflow.

```
POST https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/create-transcript-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/create-transcript-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud QA Flag",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/create-transcript-property', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud QA Flag",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of this property. Example: `MindCloud QA Flag`. |
| `type` | string | yes | The type of value held by this property. Example: `string`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Voiceflow API returns.

## Native endpoint

Through the native Voiceflow API, this operation is `POST https://analytics-api.voiceflow.com/v1/transcript-property` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transcript-property.md) for the provider-specific parameters and requirements.

