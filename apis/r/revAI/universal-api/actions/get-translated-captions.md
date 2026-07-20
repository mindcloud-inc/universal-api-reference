# Rev AI: Get Translated Captions

Retrieves translated captions from Rev AI.

```
GET https://connect.mindcloud.co/v1/universal/revAI/latest/actions/get-translated-captions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rev AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revAI/latest/actions/get-translated-captions?connectionId=$CONNECTION_ID&id=string&language=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "language": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/revAI/latest/actions/get-translated-captions?${params}`, {
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
| `id` | string | yes |  |
| `language` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `text` | string | Raw SRT caption text returned by Rev AI when the Accept header is application/x-subrip. |

## Native endpoint

Through the native Rev AI API, this operation is `GET /speechtotext/v1/jobs/:id/captions/translation/:language` (base URL `https://api.rev.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-translated-captions.md) for the provider-specific parameters and requirements.

