# QDS: List Surveys



```
GET https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-surveys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QDS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-surveys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-surveys?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "surveys": [
        {
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `surveys[].client_id` | number |  |
| `surveys[].client_name` | string |  |
| `surveys[].comment` | string |  |
| `surveys[].created_at` | date |  |
| `surveys[].deleted_at` | date |  |
| `surveys[].email_status` | string |  |
| `surveys[].employee_names` | string |  |
| `surveys[].expiration_date` | date |  |
| `surveys[].id` | number |  |
| `surveys[].image_path` | string |  |
| `surveys[].images_viewed` | number |  |
| `surveys[].job_id` | string |  |
| `surveys[].link` | string |  |
| `surveys[].processed_tips` | date |  |
| `surveys[].qa_comment` | string |  |
| `surveys[].resend_on` | date |  |
| `surveys[].resend_type` | string |  |
| `surveys[].resends_enabled` | boolean |  |
| `surveys[].resent_date` | date |  |
| `surveys[].resent_date_2` | date |  |
| `surveys[].response_date` | date |  |
| `surveys[].score` | number |  |
| `surveys[].send_on` | date |  |
| `surveys[].sent_date` | date |  |
| `surveys[].service_date` | date |  |
| `surveys[].status` | string |  |
| `surveys[].times_to_resend` | number |  |
| `surveys[].tips` | number |  |
| `surveys[].type` | string |  |
| `surveys[].updated_at` | date |  |

## Native endpoint

Through the native QDS API, this operation is `GET /surveys` (base URL `https://qdsapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-surveys.md) for the provider-specific parameters and requirements.

