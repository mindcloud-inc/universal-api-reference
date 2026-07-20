# QDS: Get Client

Retrieves a client from QDS by ID.

```
GET https://connect.mindcloud.co/v1/universal/qDS/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QDS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qDS/latest/actions/get-client?connectionId=$CONNECTION_ID&clientId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qDS/latest/actions/get-client?${params}`, {
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
| `clientId` | number | yes | The QDS client ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client": {
        "branch": "string",
        "city": "string",
        "contact_number": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "deleted_at": "2026-05-07T12:00:00.000Z",
        "disable_nicejob": true,
        "email": "ava@example.com",
        "email_status": "ava@example.com",
        "first_name": "Ava",
        "id": 1,
        "last_name": "Chen",
        "last_sent_date": "2026-05-07T12:00:00.000Z",
        "mobile": "string",
        "name": "Ava Chen",
        "response_rate": 1,
        "reviewer_name": "Ava Chen",
        "sent_surveys_count": 1,
        "sms_status": "string",
        "status": "string",
        "survey_frequency": "string",
        "survey_type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client.branch` | string |  |
| `client.city` | string |  |
| `client.contact_number` | string |  |
| `client.created_at` | date |  |
| `client.deleted_at` | date |  |
| `client.disable_nicejob` | boolean |  |
| `client.email` | string |  |
| `client.email_status` | string |  |
| `client.first_name` | string |  |
| `client.id` | number |  |
| `client.last_name` | string |  |
| `client.last_sent_date` | date |  |
| `client.mobile` | string |  |
| `client.name` | string |  |
| `client.response_rate` | number |  |
| `client.reviewer_name` | string |  |
| `client.sent_surveys_count` | number |  |
| `client.sms_status` | string |  |
| `client.status` | string |  |
| `client.survey_frequency` | string |  |
| `client.survey_type` | string |  |

## Native endpoint

Through the native QDS API, this operation is `GET /clients/:clientId` (base URL `https://qdsapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

