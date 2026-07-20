# Avoma: Get Meeting Segments

Retrieves segments for a meeting from Avoma.

```
GET https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-meeting-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avoma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-meeting-segments?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-meeting-segments?${params}`, {
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
| `uuid` | string | yes | Unique ID of the meeting. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "intro": [
        1
      ],
      "meeting": [
        1
      ],
      "overview": [
        1
      ],
      "pricing": [
        1
      ],
      "speakerSegments": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `intro` | array<number> |  |
| `meeting` | array<number> |  |
| `overview` | array<number> |  |
| `pricing` | array<number> |  |
| `speakerSegments` | object |  |

## Native endpoint

Through the native Avoma API, this operation is `GET /v1/meeting_segments/` (base URL `https://api.avoma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-meeting-segments.md) for the provider-specific parameters and requirements.

