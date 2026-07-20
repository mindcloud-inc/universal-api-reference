# MoreApp: Invite User

Invites a user to MoreApp.

```
POST https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/invite-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/invite-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "209321",
  "emailAddress": "mindcloud-moreapp-test@example.com",
  "language": "en"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/invite-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "209321",
    "emailAddress": "mindcloud-moreapp-test@example.com",
    "language": "en"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes | MoreApp customer identifier. Default: `209321`. |
| `emailAddress` | string | yes | Email address to invite. Default: `mindcloud-moreapp-test@example.com`. |
| `language` | string | yes | Invite language code. Default: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string | Empty response body on successful invite creation; presence indicates the request completed. |

## Native endpoint

Through the native MoreApp API, this operation is `POST /api/v2/customers/{{customerId}}/invites` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-user.md) for the provider-specific parameters and requirements.

