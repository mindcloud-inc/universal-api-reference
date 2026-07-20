# GAN.AI: List Sound Effect History

Retrieves sound effect generation history from GAN.AI.

```
GET https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-sound-effect-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-sound-effect-history?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-sound-effect-history?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "generationParams": {
        "creativity": 1,
        "durationSeconds": 1,
        "seed": "string"
      },
      "inferenceId": "string",
      "sfxPrompt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `generationParams.creativity` | number |  |
| `generationParams.durationSeconds` | number |  |
| `generationParams.seed` | string |  |
| `inferenceId` | string |  |
| `sfxPrompt` | string |  |

## Native endpoint

Through the native GAN.AI API, this operation is `GET /v1/sfx/history` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sound-effect-history.md) for the provider-specific parameters and requirements.

