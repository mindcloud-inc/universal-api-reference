# Groq: Delete Fine Tuning

Deletes a fine-tuning job from Groq.

```
DELETE https://connect.mindcloud.co/v1/universal/groq/latest/actions/delete-fine-tuning
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Groq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/groq/latest/actions/delete-fine-tuning?connectionId=$CONNECTION_ID&fineTuningId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fineTuningId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/groq/latest/actions/delete-fine-tuning?${params}`, {
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
      "deleted": true,
      "id": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `id` | string |  |
| `object` | string |  |

## Native endpoint

Through the native Groq API, this operation is `DELETE /v1/fine_tunings/:id` (base URL `https://api.groq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-fine-tuning.md) for the provider-specific parameters and requirements.

