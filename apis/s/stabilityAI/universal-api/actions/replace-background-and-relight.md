# Stability AI: Replace Background And Relight

Updates an image in Stability AI with background replacement.

```
PUT https://connect.mindcloud.co/v1/universal/stabilityAI/latest/actions/replace-background-and-relight
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stability AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stabilityAI/latest/actions/replace-background-and-relight" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject_image": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stabilityAI/latest/actions/replace-background-and-relight', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject_image": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subject_image` | file | yes | Subject image file to place into the new background and lighting context. |
| `backgroundPrompt` | string | no | Text prompt describing the desired generated background. Provide this when not using a background reference image. |

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
| `id` | string | Asynchronous generation result identifier. |

## Native endpoint

Through the native Stability AI API, this operation is `POST /v2beta/stable-image/edit/replace-background-and-relight` (base URL `https://api.stability.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-background-and-relight.md) for the provider-specific parameters and requirements.

