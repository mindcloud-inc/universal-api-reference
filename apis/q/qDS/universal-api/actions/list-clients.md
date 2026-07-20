# QDS: List Clients

Retrieves a list of clients from QDS.

```
GET https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QDS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-clients?${params}`, {
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
      "clients": [
        {
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clients[].branch` | string |  |
| `clients[].city` | string |  |
| `clients[].contact_number` | string |  |
| `clients[].created_at` | date |  |
| `clients[].deleted_at` | date |  |
| `clients[].disable_nicejob` | boolean |  |
| `clients[].email` | string |  |
| `clients[].email_status` | string |  |
| `clients[].first_name` | string |  |
| `clients[].id` | number |  |
| `clients[].last_name` | string |  |
| `clients[].last_sent_date` | date |  |
| `clients[].mobile` | string |  |
| `clients[].name` | string |  |
| `clients[].response_rate` | number |  |
| `clients[].reviewer_name` | string |  |
| `clients[].sent_surveys_count` | number |  |
| `clients[].sms_status` | string |  |
| `clients[].status` | string |  |
| `clients[].survey_frequency` | string |  |
| `clients[].survey_type` | string |  |

## Native endpoint

Through the native QDS API, this operation is `GET /clients` (base URL `https://qdsapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

