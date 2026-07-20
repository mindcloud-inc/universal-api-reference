# SuperSend: Create Placement Test

Creates a new placement test in SuperSend.

```
POST https://connect.mindcloud.co/v1/universal/superSend/latest/actions/create-placement-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/create-placement-test" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superSend/latest/actions/create-placement-test', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Default: Untitled Test. |
| `testEmailSubject` | string | no |  |
| `testEmailBody` | string | no | HTML body of the test email to send |
| `testEmailFrom` | string | no |  |
| `seedCount` | number | no | Default: 10. Range: 1 to 50. |
| `senderId` | string | no |  |
| `autoSend` | boolean | no | Default: false. |
| `teamId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auto_send": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "credit_cost": 1,
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "seed_addresses": [
        {
          "email": "ava@example.com"
        }
      ],
      "sender_id": "string",
      "status": "string",
      "team_id": "string",
      "total_seeds": 1,
      "tracking_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auto_send` | boolean |  |
| `created_at` | date |  |
| `credit_cost` | number |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `seed_addresses[].email` | string |  |
| `sender_id` | string |  |
| `status` | string |  |
| `team_id` | string |  |
| `total_seeds` | number |  |
| `tracking_code` | string |  |

## Native endpoint

Through the native SuperSend API, this operation is `POST /placement-tests` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-placement-test.md) for the provider-specific parameters and requirements.

