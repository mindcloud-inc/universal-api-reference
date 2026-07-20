# BuildBetter: List Calls by Participant Email



```
GET https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-calls-by-participant-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BuildBetter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-calls-by-participant-email?connectionId=$CONNECTION_ID&email=alex%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "alex@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-calls-by-participant-email?${params}`, {
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
| `email` | string | yes | Email address of the participant to match on the call attendees. Example: `alex@example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Maximum number of calls to return. Default: `25`. |

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
      "short_summary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendees` | array<object> | Matched call attendees. |
| `display_ts` | date | Display timestamp for the call. |
| `id` | string | BuildBetter call identifier. |
| `name` | string | Call title. |
| `short_summary` | string | Brief AI summary. |

## Native endpoint

Through the native BuildBetter API, this operation is `POST /graphql` (base URL `https://api.buildbetter.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calls-by-participant-email.md) for the provider-specific parameters and requirements.

