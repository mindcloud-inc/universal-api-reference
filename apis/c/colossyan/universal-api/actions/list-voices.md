# Colossyan: List Voices

Retrieves available voices from Colossyan.

```
GET https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/list-voices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Colossyan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/list-voices?${params}`, {
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
      "ages": [
        "string"
      ],
      "characters": [
        "string"
      ],
      "displayName": "Ava Chen",
      "features": {},
      "genders": [
        "string"
      ],
      "isClonedVoice": true,
      "languages": [
        "string"
      ],
      "name": "Ava Chen",
      "sample": "string",
      "scenarios": [
        "string"
      ],
      "style": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ages` | array<string> | Reported age ranges. |
| `characters` | array<string> | Character or tone descriptors. |
| `displayName` | string | Human-readable voice name. |
| `features` | object | Feature-capability flags such as pitch and speed support. |
| `genders` | array<string> | Reported voice genders. |
| `isClonedVoice` | boolean | Whether the voice is a cloned/custom voice. |
| `languages` | array<string> | Supported language codes. |
| `name` | string | Workspace voice identifier. |
| `sample` | string | Preview audio sample URL for the voice. |
| `scenarios` | array<string> | Suggested usage scenarios. |
| `style` | string | Voice style label. |

## Native endpoint

Through the native Colossyan API, this operation is `GET /assets/voices` (base URL `https://app.colossyan.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-voices.md) for the provider-specific parameters and requirements.

