# Survicate: List Respondent Responses

Retrieves responses from a specific Survicate respondent.

```
GET https://connect.mindcloud.co/v1/universal/survicate/latest/actions/list-respondent-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Survicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/survicate/latest/actions/list-respondent-responses?connectionId=$CONNECTION_ID&respondentUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "respondentUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/survicate/latest/actions/list-respondent-responses?${params}`, {
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
| `respondentUuid` | string | yes | The unique UUID of the respondent whose responses are being requested. |
| `start` | string | no | Include responses collected before this ISO 8601 timestamp with microseconds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {
        "answers": [
          {}
        ],
        "collectedAt": "2026-05-07T12:00:00.000Z",
        "deviceType": "string",
        "language": "string",
        "operatingSystem": "string",
        "respondent": {
          "attributes": [
            {}
          ],
          "uuid": "string"
        },
        "url": "https://example.com",
        "uuid": "string"
      },
      "survey": {
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response.answers` | array<object> | Answers submitted in the response. |
| `response.collectedAt` | date | Timestamp when the response was collected. |
| `response.deviceType` | string | Type of device used by the respondent. |
| `response.language` | string | Language shown to the respondent. |
| `response.operatingSystem` | string | Operating system used by the respondent. |
| `response.respondent.attributes` | array<object> | Respondent attributes included with the response. |
| `response.respondent.uuid` | string | Unique identifier of the respondent. |
| `response.url` | string | URL where the survey was displayed. |
| `response.uuid` | string | Unique identifier of the response. |
| `survey.id` | string | Unique identifier of the survey. |
| `survey.name` | string | Name of the survey. |
| `survey.type` | string | Type of the survey. |

## Native endpoint

Through the native Survicate API, this operation is `GET /respondents/:respondent_uuid/responses` (base URL `https://data-api.survicate.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-respondent-responses.md) for the provider-specific parameters and requirements.

