# BuildBetter: Get Call Details With Participants



```
GET https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/get-call-details-with-participants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BuildBetter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/get-call-details-with-participants?connectionId=$CONNECTION_ID&id=12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/get-call-details-with-participants?${params}`, {
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
| `id` | string | yes | BuildBetter call identifier. Example: `12345`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attendees": [
        {}
      ],
      "display_ts": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "short_summary": "string",
      "summary": "string",
      "transcript_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendees` | array<object> | Participants linked to the call. |
| `display_ts` | date | Display timestamp for the call. |
| `id` | string | BuildBetter call identifier. |
| `name` | string | Call title. |
| `short_summary` | string | Brief AI summary. |
| `summary` | string | Full AI summary. |
| `transcript_status` | string | Transcript processing status. |

## Native endpoint

Through the native BuildBetter API, this operation is `POST /graphql` (base URL `https://api.buildbetter.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call-details-with-participants.md) for the provider-specific parameters and requirements.

