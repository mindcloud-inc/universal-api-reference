# SurveySparrow: List Responses

Retrieves all responses from SurveySparrow.

```
GET https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/list-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveySparrow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/list-responses?connectionId=$CONNECTION_ID&limit=25&offset=0&surveyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "surveyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/list-responses?${params}`, {
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
| `surveyId` | number | yes | ID of the survey. |
| `state` | list | no | Filter responses by submission state. One of: `0`, `1`, `2`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | number | no | Filter responses by contact ID. |
| `orderBy` | list | no | Field to sort responses by. One of: `0`, `1`, `2`. |
| `order` | list | no | Sort direction. One of: `0`, `1`. |
| `preserveFormat` | boolean | no | Preserve formatted response values. |
| `responseUrl` | boolean | no | Include response URLs. |
| `dateGte` | date | no | Filter responses by completion date on or after this date. |
| `dateLte` | date | no | Filter responses by completion date on or before this date. |
| `createdDateGte` | date | no | Filter responses created on or after this date. |
| `createdDateLte` | date | no | Filter responses created on or before this date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answers": [
        {}
      ],
      "contact_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "response_id": 1,
      "response_url": "https://example.com",
      "state": "string",
      "survey_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answers` | array<object> |  |
| `contact_id` | number |  |
| `created_at` | date |  |
| `id` | number |  |
| `response_id` | number |  |
| `response_url` | string |  |
| `state` | string |  |
| `survey_id` | number |  |

## Native endpoint

Through the native SurveySparrow API, this operation is `GET /responses` (base URL `https://api.surveysparrow.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-responses.md) for the provider-specific parameters and requirements.

