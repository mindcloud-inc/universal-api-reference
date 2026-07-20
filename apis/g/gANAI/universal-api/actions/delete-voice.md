# GAN.AI: Delete Voice

Deletes an existing voice from GAN.AI.

```
DELETE https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/delete-voice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/delete-voice?connectionId=$CONNECTION_ID&voice_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "voice_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/delete-voice?${params}`, {
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
| `voice_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native GAN.AI API, this operation is `DELETE /v1/voices/[:voice_id]` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-voice.md) for the provider-specific parameters and requirements.

