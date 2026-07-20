# Speak Ai: Delete Media

Deletes an existing media item from Speak Ai.

```
DELETE https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/delete-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Speak Ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/delete-media?connectionId=$CONNECTION_ID&mediaId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mediaId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/delete-media?${params}`, {
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
| `mediaId` | string | yes | Speak Ai media identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Speak Ai API, this operation is `DELETE /media/:mediaId` (base URL `https://api.speakai.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-media.md) for the provider-specific parameters and requirements.

