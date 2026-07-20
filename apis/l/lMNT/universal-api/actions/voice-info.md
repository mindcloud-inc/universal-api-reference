# LMNT: Voice Info

Retrieves details for a specific voice from LMNT.

```
GET https://connect.mindcloud.co/v1/universal/lMNT/latest/actions/voice-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LMNT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lMNT/latest/actions/voice-info?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lMNT/latest/actions/voice-info?${params}`, {
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
| `id` | string | yes | The id of the voice. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "gender": "string",
      "id": "string",
      "name": "Ava Chen",
      "owner": "string",
      "preview_url": "https://example.com",
      "starred": true,
      "state": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gender` | string |  |
| `id` | string |  |
| `name` | string |  |
| `owner` | string |  |
| `preview_url` | string |  |
| `starred` | boolean |  |
| `state` | string |  |
| `type` | string |  |

## Native endpoint

Through the native LMNT API, this operation is `GET /v1/ai/voice/:id` (base URL `https://api.lmnt.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/voice-info.md) for the provider-specific parameters and requirements.

