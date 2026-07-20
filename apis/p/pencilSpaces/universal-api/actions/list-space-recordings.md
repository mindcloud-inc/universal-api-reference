# Pencil Spaces: List Space Recordings



```
GET https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/list-space-recordings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pencil Spaces `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/list-space-recordings?connectionId=$CONNECTION_ID&spaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/list-space-recordings?${params}`, {
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
| `spaceId` | string | yes | The Space whose recordings you want to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration": 1,
      "fileSize": 1,
      "recordingId": "string",
      "roomId": "string",
      "spaceId": "string",
      "startingTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duration` | number |  |
| `fileSize` | number |  |
| `recordingId` | string |  |
| `roomId` | string |  |
| `spaceId` | string |  |
| `startingTime` | string |  |

## Native endpoint

Through the native Pencil Spaces API, this operation is `GET /spaces/recordings/:spaceId` (base URL `https://apis.pencilapp.com/public/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-space-recordings.md) for the provider-specific parameters and requirements.

