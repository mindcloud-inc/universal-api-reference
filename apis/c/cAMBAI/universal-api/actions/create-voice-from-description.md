# CAMB.AI: Create Voice from Description

Creates a new voice from a description in CAMB.AI.

```
POST https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/create-voice-from-description
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CAMB.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/create-voice-from-description" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "string",
  "voiceDescription": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/create-voice-from-description', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "string",
    "voiceDescription": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | yes | Sample text the generated voice should speak. |
| `voiceDescription` | string | yes | Detailed description of the desired voice characteristics. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "task_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `task_id` | string | Task identifier for the voice generation request. |

## Native endpoint

Through the native CAMB.AI API, this operation is `POST /text-to-voice` (base URL `https://client.camb.ai/apis`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-voice-from-description.md) for the provider-specific parameters and requirements.

