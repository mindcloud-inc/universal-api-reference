# Vibrato: Retrieve call

Retrieves a specific call from Vibrato.

```
GET https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/retrieve-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vibrato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/retrieve-call?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/retrieve-call?${params}`, {
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
| `id` | string | yes | ID of the call. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "api_idempotency_key": "string",
      "completed_at": "2026-05-07T12:00:00.000Z",
      "country_code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "id": 1,
      "labels": [
        "string"
      ],
      "language_name": "Ava Chen",
      "locale": "string",
      "locale_name": "Ava Chen",
      "phone_number": "string",
      "prompt": "string",
      "recording_url": "https://example.com",
      "started_at": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "succeeded": true,
      "summary": "string",
      "tags": [
        "string"
      ],
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_idempotency_key` | string |  |
| `completed_at` | date |  |
| `country_code` | string |  |
| `created_at` | date |  |
| `duration` | number |  |
| `id` | number |  |
| `labels` | array<string> |  |
| `language_name` | string |  |
| `locale` | string |  |
| `locale_name` | string |  |
| `phone_number` | string |  |
| `prompt` | string |  |
| `recording_url` | string |  |
| `started_at` | date |  |
| `status` | string |  |
| `succeeded` | boolean |  |
| `summary` | string |  |
| `tags` | array<string> |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Vibrato API, this operation is `GET /calls/{id}/` (base URL `https://api.getvibrato.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-call.md) for the provider-specific parameters and requirements.

