# Voiceflow: Set Transcript Property Value

Sets a transcript property value in Voiceflow.

```
POST https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/set-transcript-property-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/set-transcript-property-value" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "propertyId": "prop_1234567890",
  "transcriptId": "transcript_1234567890",
  "value": "pass"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/set-transcript-property-value', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "propertyId": "prop_1234567890",
    "transcriptId": "transcript_1234567890",
    "value": "pass"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `propertyId` | string | yes | ID of the transcript property to target. Example: `prop_1234567890`. |
| `transcriptId` | string | yes | ID of the transcript to target. Example: `transcript_1234567890`. |
| `value` | string | yes | Value of the transcript property to set. Example: `pass`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | object | no | Additional metadata associated with the property value. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Voiceflow API returns.

## Native endpoint

Through the native Voiceflow API, this operation is `POST https://analytics-api.voiceflow.com/v1/transcript-property-value` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-transcript-property-value.md) for the provider-specific parameters and requirements.

