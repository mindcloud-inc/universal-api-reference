# SatisMeter: List Project Responses



```
GET https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/list-project-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SatisMeter `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/list-project-responses?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=61fce0adea447e24ec27d606" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "61fce0adea447e24ec27d606"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/list-project-responses?${params}`, {
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
| `endDate` | date | no | Filter responses recorded before this ISO 8601 timestamp. Example: `2026-03-17T23:59:59Z`. |
| `projectId` | string | yes | Project ID. Example: `61fce0adea447e24ec27d606`. |
| `startDate` | date | no | Filter responses recorded after this ISO 8601 timestamp. Example: `2026-03-01T00:00:00Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answers": [
        {
          "id": "string",
          "label": "string",
          "metric": "string",
          "name": "Ava Chen",
          "type": "string",
          "value": "string"
        }
      ],
      "campaign": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "device": {
        "type": "string"
      },
      "id": "string",
      "language": "string",
      "location": {
        "city": "string",
        "country": {
          "code": "string",
          "name": "Ava Chen"
        },
        "region": {
          "code": "string",
          "name": "Ava Chen"
        }
      },
      "method": "string",
      "project": "string",
      "user": {
        "deleted": true,
        "id": "string",
        "userId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answers` | array<object> | Recorded answers for the response. |
| `answers[].id` | string | Question ID. |
| `answers[].label` | string | Question label. |
| `answers[].metric` | string | Metric type when provided. |
| `answers[].name` | string | Provider answer token. |
| `answers[].type` | string | Question type. |
| `answers[].value` | string | Question answer value. SatisMeter may return strings or numbers depending on question type. |
| `campaign` | string | Survey ID. |
| `created` | date | Response creation timestamp. |
| `device` | object | Device summary. |
| `device.type` | string | Device type. |
| `id` | string | Response ID. |
| `language` | string | Response language. |
| `location` | object | Location summary. |
| `location.city` | string | City. |
| `location.country` | object | Country summary. |
| `location.country.code` | string | Country code. |
| `location.country.name` | string | Country name. |
| `location.region` | object | Region summary. |
| `location.region.code` | string | Region code. |
| `location.region.name` | string | Region name. |
| `method` | string | Survey delivery method. |
| `project` | string | Project ID. |
| `user` | object | Associated user summary. |
| `user.deleted` | boolean | Whether the user has been anonymized or deleted. |
| `user.id` | string | SatisMeter internal user ID. |
| `user.userId` | string | External user ID. |

## Native endpoint

Through the native SatisMeter API, this operation is `GET /api/v3/projects/:projectId/responses` (base URL `https://app.satismeter.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-responses.md) for the provider-specific parameters and requirements.

