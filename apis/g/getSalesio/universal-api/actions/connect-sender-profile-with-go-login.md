# GetSales.io: Connect Sender Profile With GoLogin



```
PUT https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/connect-sender-profile-with-go-login
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetSales.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/connect-sender-profile-with-go-login" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "John",
  "lastName": "Doe",
  "gologinExternalId": "gl-profile-123456"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/connect-sender-profile-with-go-login', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "John",
    "lastName": "Doe",
    "gologinExternalId": "gl-profile-123456"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | First name of the sender. Example: `John`. |
| `lastName` | string | yes | Last name of the sender. Example: `Doe`. |
| `label` | string | no | Optional custom label for identification. Example: `Main LinkedIn Profile`. |
| `gologinExternalId` | string | yes | External ID from GoLogin used to create the browser profile. Example: `gl-profile-123456`. |
| `schedule` | object | no | Schedule object with timezone and timeblocks. Example: `[object Object]`. |
| `smartLimitsEnabled` | boolean | no | Enables smart limits for automation. |
| `notificationEmails[]` | array<string> | no | Notification email addresses. Example: `alerts@example.com`. |
| `browserOwner` | string | no | Optional owner of the browser profile. Example: `customer`. |

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

Through the native GetSales.io API, this operation is `POST /flows/client-api/sender-profiles/connect-external` (base URL `https://amazing.getsales.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/connect-sender-profile-with-go-login.md) for the provider-specific parameters and requirements.

