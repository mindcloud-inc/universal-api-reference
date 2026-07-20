# Maildrip: Import CSV contacts to an instant email



```
POST https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/import-csv-contacts-to-an-instant-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/import-csv-contacts-to-an-instant-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "draftEmailId": "ava@example.com",
  "contacts[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/import-csv-contacts-to-an-instant-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "draftEmailId": "ava@example.com",
    "contacts[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `draftEmailId` | string | yes | ID of the instant email to import contacts into |
| `contacts[]` | array<object> | yes | Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "failed_uploads": 1,
      "jobType": 1,
      "message": "string",
      "processed": 1,
      "stats": {},
      "status": 1,
      "successful_uploads": 1,
      "total": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `createdAt` | date |  |
| `failed_uploads` | number |  |
| `jobType` | number |  |
| `message` | string |  |
| `processed` | number |  |
| `stats` | object |  |
| `status` | number |  |
| `successful_uploads` | number |  |
| `total` | number |  |
| `updatedAt` | date |  |
| `user` | string |  |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/instant-emails/upload/{emailId}` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-csv-contacts-to-an-instant-email.md) for the provider-specific parameters and requirements.

