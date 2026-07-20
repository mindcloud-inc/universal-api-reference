# Survicate: Get Survey

Retrieves a specific survey from Survicate.

```
GET https://connect.mindcloud.co/v1/universal/survicate/latest/actions/get-survey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Survicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/survicate/latest/actions/get-survey?connectionId=$CONNECTION_ID&surveyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/survicate/latest/actions/get-survey?${params}`, {
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
| `surveyId` | string | yes | The unique identifier of the survey to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {
        "email": "ava@example.com",
        "name": "Ava Chen"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "firstResponseAt": "2026-05-07T12:00:00.000Z",
      "folder": "string",
      "id": "string",
      "lastResponseAt": "2026-05-07T12:00:00.000Z",
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
| `author.email` | string | Email of the survey author. |
| `author.name` | string | Name of the survey author. |
| `createdAt` | date | Timestamp when the survey was created. |
| `enabled` | boolean | Whether the survey is currently enabled. |
| `firstResponseAt` | date | Timestamp of the first collected response. |
| `folder` | string | Folder containing the survey. |
| `id` | string | Unique identifier of the survey. |
| `lastResponseAt` | date | Timestamp of the most recent collected response. |
| `launch.endAt` | date | Scheduled survey end time, if any. |
| `launch.responsesLimit` | number | Maximum responses allowed before the survey stops. |
| `launch.startAt` | date | Scheduled survey start time, if any. |
| `name` | string | Survey name. |
| `responses` | number | Total number of responses collected. |
| `type` | string | Immutable survey type. |

## Native endpoint

Through the native Survicate API, this operation is `GET /surveys/:survey_id` (base URL `https://data-api.survicate.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey.md) for the provider-specific parameters and requirements.

