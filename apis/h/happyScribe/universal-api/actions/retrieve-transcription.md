# HappyScribe: Retrieve Transcription

Retrieves a transcription from HappyScribe.

```
GET https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/retrieve-transcription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HappyScribe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/retrieve-transcription?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/retrieve-transcription?${params}`, {
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
| `id` | string | yes | The transcription identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "audioLengthInSeconds": 1,
      "id": "string",
      "language": "string",
      "name": "Ava Chen",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object |  |
| `audioLengthInSeconds` | number |  |
| `id` | string |  |
| `language` | string |  |
| `name` | string |  |
| `state` | string |  |

## Native endpoint

Through the native HappyScribe API, this operation is `GET /transcriptions/:id` (base URL `https://www.happyscribe.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-transcription.md) for the provider-specific parameters and requirements.

