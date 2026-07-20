# Murf Core: List Voices

Retrieves available voices from Murf Core.

```
GET https://connect.mindcloud.co/v1/universal/murfCore/latest/actions/list-voices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Murf Core `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/murfCore/latest/actions/list-voices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/murfCore/latest/actions/list-voices?${params}`, {
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
| `model` | string | no | Optional Murf voice model filter. Valid values are FALCON or GEN2. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accent": "string",
      "availableStyles": [
        "string"
      ],
      "description": "string",
      "displayLanguage": "string",
      "displayName": "Ava Chen",
      "gender": "string",
      "locale": "string",
      "supportedLocales": {},
      "voiceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accent` | string | Accent label returned by Murf. |
| `availableStyles` | array<string> | Available speaking styles for the voice. |
| `description` | string | Age-range description for the voice. |
| `displayLanguage` | string | Display language for the voice. |
| `displayName` | string | Human-readable voice name. |
| `gender` | string | Voice gender. |
| `locale` | string | Primary locale for the voice. |
| `supportedLocales` | object | Map of supported locales and their styles. |
| `voiceId` | string | Unique Murf voice identifier. |

## Native endpoint

Through the native Murf Core API, this operation is `GET /v1/speech/voices` (base URL `https://api.murf.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-voices.md) for the provider-specific parameters and requirements.

