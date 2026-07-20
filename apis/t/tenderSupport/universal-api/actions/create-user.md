# Tender Support: Create User

Creates a new user in Tender Support.

```
POST https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tender Support `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "password": "string",
  "passwordConfirmation": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "password": "string",
    "passwordConfirmation": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The user's email address. |
| `password` | string | yes | The user's password. |
| `passwordConfirmation` | string | yes | The password confirmation. |
| `name` | string | no | The user's name. |
| `title` | string | no | The user's job title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activatedAt": "2026-05-07T12:00:00.000Z",
      "commentsCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "discussionsCount": 1,
      "discussionsHref": "string",
      "email": "ava@example.com",
      "enableEmailNotifications": true,
      "externalId": "string",
      "href": "string",
      "name": "Ava Chen",
      "openidUrl": "https://example.com",
      "publicFacing": true,
      "state": "string",
      "title": "string",
      "trusted": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activatedAt` | date |  |
| `commentsCount` | number |  |
| `createdAt` | date |  |
| `discussionsCount` | number |  |
| `discussionsHref` | string |  |
| `email` | string |  |
| `enableEmailNotifications` | boolean |  |
| `externalId` | string |  |
| `href` | string |  |
| `name` | string |  |
| `openidUrl` | string |  |
| `publicFacing` | boolean |  |
| `state` | string |  |
| `title` | string |  |
| `trusted` | boolean |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Tender Support API, this operation is `POST /users` (base URL `https://api.tenderapp.com/help`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

