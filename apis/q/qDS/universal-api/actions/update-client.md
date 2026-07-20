# QDS: Update Client



```
PUT https://connect.mindcloud.co/v1/universal/qDS/latest/actions/update-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QDS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/qDS/latest/actions/update-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qDS/latest/actions/update-client', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | number | yes | The QDS client ID. |
| `client.name` | string | no | Client display name. |
| `client.firstName` | string | no | Client first name. |
| `client.lastName` | string | no | Client last name. |
| `client.email` | string | no | Client email address. |
| `client.reviewerName` | string | no | Reviewer display name. |
| `client.city` | string | no | Client city. |
| `client.branch` | string | no | Branch or location. |
| `client.mobile` | string | no | Mobile phone number. |
| `client.contactNumber` | string | no | Contact phone number. |
| `client.surveyFrequency` | string | no | Survey cadence setting. |
| `client.surveyType` | string | no | Survey type setting. |
| `client.disableNicejob` | boolean | no | Whether NiceJob is disabled for the client. |
| `client.status` | string | no | Client status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client": {
        "branch_id": 1,
        "city": "string",
        "contact_number": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "deleted_at": "2026-05-07T12:00:00.000Z",
        "disable_nicejob": 1,
        "email": "ava@example.com",
        "email_status": "ava@example.com",
        "external_id": "string",
        "first_name": "Ava",
        "id": 1,
        "last_name": "Chen",
        "mobile": "string",
        "name": "Ava Chen",
        "nicejob_client_id": "string",
        "reviewer_name": "Ava Chen",
        "sms_status": "string",
        "status": "string",
        "survey_frequency": "string",
        "survey_type": "string",
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
| `client.branch_id` | number |  |
| `client.city` | string |  |
| `client.contact_number` | string |  |
| `client.created_at` | date |  |
| `client.deleted_at` | date |  |
| `client.disable_nicejob` | number |  |
| `client.email` | string |  |
| `client.email_status` | string |  |
| `client.external_id` | string |  |
| `client.first_name` | string |  |
| `client.id` | number |  |
| `client.last_name` | string |  |
| `client.mobile` | string |  |
| `client.name` | string |  |
| `client.nicejob_client_id` | string |  |
| `client.reviewer_name` | string |  |
| `client.sms_status` | string |  |
| `client.status` | string |  |
| `client.survey_frequency` | string |  |
| `client.survey_type` | string |  |
| `client.updated_at` | date |  |

## Native endpoint

Through the native QDS API, this operation is `PUT /clients/:clientId` (base URL `https://qdsapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client.md) for the provider-specific parameters and requirements.

