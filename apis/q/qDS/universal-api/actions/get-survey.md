# QDS: Get Survey



```
GET https://connect.mindcloud.co/v1/universal/qDS/latest/actions/get-survey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QDS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qDS/latest/actions/get-survey?connectionId=$CONNECTION_ID&surveyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qDS/latest/actions/get-survey?${params}`, {
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
| `surveyId` | number | yes | The QDS survey ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "survey": {
        "client_id": 1,
        "client_name": "Ava Chen",
        "comment": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "deleted_at": "2026-05-07T12:00:00.000Z",
        "email_status": "ava@example.com",
        "employee_names": "Ava Chen",
        "expiration_date": "2026-05-07T12:00:00.000Z",
        "id": 1,
        "image_path": "string",
        "images_viewed": 1,
        "job_id": "string",
        "link": "https://example.com",
        "processed_tips": "2026-05-07T12:00:00.000Z",
        "qa_comment": "string",
        "resend_on": "2026-05-07T12:00:00.000Z",
        "resend_type": "string",
        "resends_enabled": true,
        "resent_date": "2026-05-07T12:00:00.000Z",
        "resent_date_2": "2026-05-07T12:00:00.000Z",
        "response_date": "2026-05-07T12:00:00.000Z",
        "score": 1,
        "send_on": "2026-05-07T12:00:00.000Z",
        "sent_date": "2026-05-07T12:00:00.000Z",
        "service_date": "2026-05-07T12:00:00.000Z",
        "status": "string",
        "times_to_resend": 1,
        "tips": 1,
        "type": "string",
        "updated_at": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `survey.client_id` | number |  |
| `survey.client_name` | string |  |
| `survey.comment` | string |  |
| `survey.created_at` | date |  |
| `survey.deleted_at` | date |  |
| `survey.email_status` | string |  |
| `survey.employee_names` | string |  |
| `survey.expiration_date` | date |  |
| `survey.id` | number |  |
| `survey.image_path` | string |  |
| `survey.images_viewed` | number |  |
| `survey.job_id` | string |  |
| `survey.link` | string |  |
| `survey.processed_tips` | date |  |
| `survey.qa_comment` | string |  |
| `survey.resend_on` | date |  |
| `survey.resend_type` | string |  |
| `survey.resends_enabled` | boolean |  |
| `survey.resent_date` | date |  |
| `survey.resent_date_2` | date |  |
| `survey.response_date` | date |  |
| `survey.score` | number |  |
| `survey.send_on` | date |  |
| `survey.sent_date` | date |  |
| `survey.service_date` | date |  |
| `survey.status` | string |  |
| `survey.times_to_resend` | number |  |
| `survey.tips` | number |  |
| `survey.type` | string |  |
| `survey.updated_at` | date |  |

## Native endpoint

Through the native QDS API, this operation is `GET /surveys/:surveyId` (base URL `https://qdsapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey.md) for the provider-specific parameters and requirements.

