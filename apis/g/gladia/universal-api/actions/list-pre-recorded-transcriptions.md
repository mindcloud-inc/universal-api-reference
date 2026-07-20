# Gladia: List Pre-recorded Transcriptions

Retrieves pre-recorded transcription jobs from Gladia.

```
GET https://connect.mindcloud.co/v1/universal/gladia/latest/actions/list-pre-recorded-transcriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gladia `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gladia/latest/actions/list-pre-recorded-transcriptions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gladia/latest/actions/list-pre-recorded-transcriptions?${params}`, {
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
| `date` | date | no | Filter items relevant to a specific date in ISO format (YYYY-MM-DD). |
| `beforeDate` | date | no | Include items that occurred before the specified date in ISO format. |
| `afterDate` | date | no | Filter for items after the specified date. Use with before_date for a range. |
| `status` | list<string> | no | Filter the list based on item status. One of: `done`, `error`, `processing`, `queued`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "current": "string",
      "first": "string",
      "items": [
        {}
      ],
      "next": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current` | string |  |
| `first` | string |  |
| `items` | array<object> |  |
| `next` | string |  |

## Native endpoint

Through the native Gladia API, this operation is `GET /v2/pre-recorded` (base URL `https://api.gladia.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pre-recorded-transcriptions.md) for the provider-specific parameters and requirements.

