# Survicate: List Surveys

Retrieves surveys from your Survicate workspace.

```
GET https://connect.mindcloud.co/v1/universal/survicate/latest/actions/list-surveys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Survicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/survicate/latest/actions/list-surveys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/survicate/latest/actions/list-surveys?${params}`, {
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
| `start` | string | no | Filter surveys created before or at this ISO 8601 timestamp with microseconds. |
| `end` | string | no | Filter surveys created on or after this ISO 8601 timestamp with microseconds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "id": "string",
      "launch": {
        "endAt": "2026-05-07T12:00:00.000Z",
        "responsesLimit": 1,
        "startAt": "2026-05-07T12:00:00.000Z"
      },
      "name": "Ava Chen",
      "responses": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Timestamp when the survey was created. |
| `enabled` | boolean | Whether the survey is currently enabled. |
| `id` | string | Unique identifier of the survey. |
| `launch.endAt` | date | Scheduled survey end time, if any. |
| `launch.responsesLimit` | number | Maximum responses allowed before the survey stops. |
| `launch.startAt` | date | Scheduled survey start time, if any. |
| `name` | string | Survey name. |
| `responses` | number | Total number of responses collected. |
| `type` | string | Immutable survey type. |

## Native endpoint

Through the native Survicate API, this operation is `GET /surveys` (base URL `https://data-api.survicate.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-surveys.md) for the provider-specific parameters and requirements.

