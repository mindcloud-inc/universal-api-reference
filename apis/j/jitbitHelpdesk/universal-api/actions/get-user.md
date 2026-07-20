# Jitbit Helpdesk: Get User



```
GET https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jitbit Helpdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/get-user?${params}`, {
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
| `userId` | number | yes | Jitbit user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": 1,
      "companyName": "Ava Chen",
      "disabled": true,
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "isAdmin": true,
      "isTech": true,
      "lastName": "Chen",
      "lastSeen": "string",
      "sendEmail": true,
      "userId": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | number | Company ID when present. |
| `companyName` | string | Company name when present. |
| `disabled` | boolean | Whether the user is disabled. |
| `email` | string | Email address. |
| `firstName` | string | First name. |
| `fullName` | string | Full name. |
| `isAdmin` | boolean | Whether the user is an administrator. |
| `isTech` | boolean | Whether the user is a technician. |
| `lastName` | string | Last name. |
| `lastSeen` | string | Last seen timestamp. |
| `sendEmail` | boolean | Whether email sending is enabled. |
| `userId` | number | User ID. |
| `username` | string | Username. |

## Native endpoint

Through the native Jitbit Helpdesk API, this operation is `GET /User` (base URL `{{credentials.helpdeskBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

