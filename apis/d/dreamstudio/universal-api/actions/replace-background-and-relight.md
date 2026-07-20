# Dreamstudio: Replace Background and Relight

Replaces an image background and relights it in Dreamstudio.

```
PUT https://connect.mindcloud.co/v1/universal/dreamstudio/latest/actions/replace-background-and-relight
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dreamstudio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dreamstudio/latest/actions/replace-background-and-relight" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subjectImage": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dreamstudio/latest/actions/replace-background-and-relight', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subjectImage": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subjectImage` | file | yes | Foreground subject image used for the background replacement job. |
| `backgroundPrompt` | string | no | Optional text describing the replacement background. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Async relight job id. |

## Native endpoint

Through the native Dreamstudio API, this operation is `POST /v2beta/stable-image/edit/replace-background-and-relight` (base URL `https://api.stability.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-background-and-relight.md) for the provider-specific parameters and requirements.

