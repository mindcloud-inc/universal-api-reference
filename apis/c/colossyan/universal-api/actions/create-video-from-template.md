# Colossyan: Create Video From Template

Creates a video generation job from a Colossyan template.

```
POST https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/create-video-from-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Colossyan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/create-video-from-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateJobId": "string",
  "dynamicVariables": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/create-video-from-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateJobId": "string",
    "dynamicVariables": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateJobId` | string | yes | ID of the Colossyan template job to execute. |
| `dynamicVariables` | object | yes | Object of template variables to inject into the template. |
| `callbackUrl` | string | no | Optional callback URL for job completion events. |
| `callbackPayload` | object | no | Optional callback payload object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "videoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created Colossyan template video generation job ID. |
| `videoId` | string | Generated video ID associated with the created template job. |

## Native endpoint

Through the native Colossyan API, this operation is `POST /video-generation-jobs/template-jobs` (base URL `https://app.colossyan.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-video-from-template.md) for the provider-specific parameters and requirements.

