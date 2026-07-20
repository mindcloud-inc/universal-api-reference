# Sales Cookie: Create Or Update User

Creates or updates a user in Sales Cookie by email address.

```
PUT https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/create-or-update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sales Cookie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/create-or-update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emailAddress": "ava@example.com",
  "role": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/create-or-update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emailAddress": "ava@example.com",
    "role": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailAddress` | string | yes | User email address used to create or update the user. |
| `role` | string | yes | Workspace role. Valid values include FullAdmin, LimitedAdmin, Participant, and Deactivated. |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `tags` | string | no | Optional pipe-delimited tags. |
| `aliases` | string | no | Optional pipe-delimited aliases. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aliases": "string",
      "currency": "string",
      "dashboardDisabled": true,
      "directManagerId": "string",
      "emailAddress": "ava@example.com",
      "endDate": "2026-05-07T12:00:00.000Z",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "role": "string",
      "startDate": "2026-05-07T12:00:00.000Z",
      "systemUserId": "string",
      "tags": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aliases` | string |  |
| `currency` | string |  |
| `dashboardDisabled` | boolean |  |
| `directManagerId` | string |  |
| `emailAddress` | string |  |
| `endDate` | date |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `role` | string |  |
| `startDate` | date |  |
| `systemUserId` | string |  |
| `tags` | string |  |

## Native endpoint

Through the native Sales Cookie API, this operation is `POST /Api/SetUser` (base URL `https://salescookie.com/app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-user.md) for the provider-specific parameters and requirements.

