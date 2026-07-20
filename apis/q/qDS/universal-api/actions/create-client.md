# QDS: Create Client



```
POST https://connect.mindcloud.co/v1/universal/qDS/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QDS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qDS/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "client.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qDS/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "client.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `client.name` | string | yes | Client display name. |
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
        "created_at": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen",
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
| `client.created_at` | date |  |
| `client.email` | string |  |
| `client.id` | number |  |
| `client.name` | string |  |
| `client.status` | string |  |
| `client.survey_frequency` | string |  |
| `client.survey_type` | string |  |
| `client.updated_at` | date |  |

## Native endpoint

Through the native QDS API, this operation is `POST /clients` (base URL `https://qdsapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

