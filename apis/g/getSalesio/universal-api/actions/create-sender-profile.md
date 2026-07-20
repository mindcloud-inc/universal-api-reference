# GetSales.io: Create Sender Profile



```
POST https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/create-sender-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetSales.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/create-sender-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/create-sender-profile', {
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
| `assigneeUserId` | number | no | ID of the user assigned to the sender profile. Example: `1`. |
| `firstName` | string | no | Sender first name. Example: `John`. |
| `lastName` | string | no | Sender last name. Example: `Doe`. |
| `label` | string | no | Custom sender profile label. Example: `USA media owners`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee_user_id": 1,
      "first_name": "Ava",
      "label": "string",
      "last_name": "Chen",
      "status": "string",
      "team_id": 1,
      "user_id": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee_user_id` | number |  |
| `first_name` | string |  |
| `label` | string |  |
| `last_name` | string |  |
| `status` | string |  |
| `team_id` | number |  |
| `user_id` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native GetSales.io API, this operation is `POST /flows/api/sender-profiles` (base URL `https://amazing.getsales.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sender-profile.md) for the provider-specific parameters and requirements.

