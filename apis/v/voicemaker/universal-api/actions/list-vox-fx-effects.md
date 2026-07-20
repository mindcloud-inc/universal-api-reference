# Voicemaker: List VoxFX Effects

Retrieves available VoxFX effects from Voicemaker.

```
GET https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/list-vox-fx-effects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voicemaker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/list-vox-fx-effects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/list-vox-fx-effects?${params}`, {
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
      "data": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `success` | boolean |  |

## Native endpoint

Through the native Voicemaker API, this operation is `GET effects/voxfx` (base URL `https://developer.voicemaker.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vox-fx-effects.md) for the provider-specific parameters and requirements.

