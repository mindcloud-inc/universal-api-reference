# SmartSurvey: List Survey Invitations

Retrieves survey invitations for a SmartSurvey survey.

```
GET https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/list-survey-invitations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSurvey `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/list-survey-invitations?connectionId=$CONNECTION_ID&limit=25&offset=0&surveyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "surveyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/list-survey-invitations?${params}`, {
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
| `surveyId` | number | yes | The survey id whose Invitations you are querying |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sentOnly` | boolean | no | A value indicating whether to return only sent invitations |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact_count": 1,
      "contact_list_id": 1,
      "date_created": "2026-05-07T12:00:00.000Z",
      "date_sent": "2026-05-07T12:00:00.000Z",
      "href": "string",
      "id": 1,
      "link_id": 1,
      "message_body": "string",
      "message_sender": "string",
      "message_sender_name": "Ava Chen",
      "message_subject": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact_count` | number |  |
| `contact_list_id` | number |  |
| `date_created` | date |  |
| `date_sent` | date |  |
| `href` | string |  |
| `id` | number |  |
| `link_id` | number |  |
| `message_body` | string |  |
| `message_sender` | string |  |
| `message_sender_name` | string |  |
| `message_subject` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native SmartSurvey API, this operation is `GET /surveys/{surveyId}/invitations` (base URL `https://api.smartsurvey.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-survey-invitations.md) for the provider-specific parameters and requirements.

