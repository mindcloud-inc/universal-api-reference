# Groq: Get Fine Tuning

Retrieves a fine-tuning job from Groq.

```
GET https://connect.mindcloud.co/v1/universal/groq/latest/actions/get-fine-tuning
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Groq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/groq/latest/actions/get-fine-tuning?connectionId=$CONNECTION_ID&fineTuningId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fineTuningId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/groq/latest/actions/get-fine-tuning?${params}`, {
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
| `fineTuningId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseModel": "string",
      "createdAt": 1,
      "fineTunedModel": "string",
      "id": "string",
      "inputFileId": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseModel` | string |  |
| `createdAt` | number |  |
| `fineTunedModel` | string |  |
| `id` | string |  |
| `inputFileId` | string |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Groq API, this operation is `GET /v1/fine_tunings/:id` (base URL `https://api.groq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fine-tuning.md) for the provider-specific parameters and requirements.

