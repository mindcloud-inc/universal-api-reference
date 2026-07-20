# IceCubes: Get Meeting Notes



```
GET https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/get-meeting-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IceCubes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/get-meeting-notes?connectionId=$CONNECTION_ID&meetingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "meetingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iceCubes/latest/actions/get-meeting-notes?${params}`, {
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
| `meetingId` | string | yes | The meeting ID to retrieve notes for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Meeting notes content. |
| `updatedAt` | date | When the notes were last updated. |
| `version` | number | Notes version number. |

## Native endpoint

Through the native IceCubes API, this operation is `GET /meetings/:id/notes` (base URL `https://icecubes.app/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-meeting-notes.md) for the provider-specific parameters and requirements.

