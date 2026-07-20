# CAMB.AI: Create Audio Separation

Creates a new audio separation task in CAMB.AI.

```
POST https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/create-audio-separation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CAMB.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/create-audio-separation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "media_file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cAMBAI/latest/actions/create-audio-separation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "media_file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `media_file` | file | yes | Audio file to separate into foreground and background components. |
| `projectName` | string | no | Optional project name shown in the CAMB.AI workspace. |
| `projectDescription` | string | no | Optional workspace description for the separation task. |
| `folderId` | number | no | Optional CAMB.AI folder identifier for storing the task. |

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
| `task_id` | string | Task identifier for the audio separation request. |

## Native endpoint

Through the native CAMB.AI API, this operation is `POST /audio-separation` (base URL `https://client.camb.ai/apis`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-audio-separation.md) for the provider-specific parameters and requirements.

