# BuildBetter: Get Signal By ID



```
GET https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/get-signal-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BuildBetter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/get-signal-by-id?connectionId=$CONNECTION_ID&id=12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/get-signal-by-id?${params}`, {
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
| `id` | string | yes | BuildBetter signal ID. Example: `12345`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "call": {},
      "context": "string",
      "display_ts": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "interview_id": "string",
      "person": {},
      "person_id": "string",
      "sentiment": 1,
      "speaker": 1,
      "summary": "string",
      "types": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `call` | object | Linked call summary. |
| `context` | string | Source context for the signal. |
| `display_ts` | date | Signal display timestamp. |
| `id` | string | BuildBetter signal identifier. |
| `interview_id` | string | Linked call identifier. |
| `person` | object | Linked person summary. |
| `person_id` | string | Linked person identifier. |
| `sentiment` | number | Signal sentiment score. |
| `speaker` | number | Speaker code for the signal. |
| `summary` | string | Signal summary text. |
| `types` | array<object> | Signal type assignments. |

## Native endpoint

Through the native BuildBetter API, this operation is `POST /graphql` (base URL `https://api.buildbetter.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signal-by-id.md) for the provider-specific parameters and requirements.

