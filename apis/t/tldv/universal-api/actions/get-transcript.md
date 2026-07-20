# tl:dv: Get Transcript

Retrieves a meeting transcript from tl:dv.

```
GET https://connect.mindcloud.co/v1/universal/tldv/latest/actions/get-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a tl:dv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tldv/latest/actions/get-transcript?connectionId=$CONNECTION_ID&meetingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "meetingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tldv/latest/actions/get-transcript?${params}`, {
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
| `meetingId` | string | yes | The tl:dv meeting identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "id": "string",
      "meetingId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Transcript segments with speaker, text, startTime, and endTime. |
| `id` | string | The transcript identifier. |
| `meetingId` | string | The related meeting identifier. |

## Native endpoint

Through the native tl:dv API, this operation is `GET /v1alpha1/meetings/:meetingId/transcript` (base URL `https://pasta.tldv.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transcript.md) for the provider-specific parameters and requirements.

