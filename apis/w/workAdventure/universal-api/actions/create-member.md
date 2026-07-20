# WorkAdventure: Create member

Creates a member in a WorkAdventure world.

```
POST https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/create-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkAdventure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/create-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "worldSlug": "string",
  "name": "Ava Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/create-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "worldSlug": "string",
    "name": "Ava Chen",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `worldSlug` | string | yes | The world slug from the WorkAdventure world URL. |
| `name` | string | yes | Name of the Woka. |
| `email` | string | yes | Email of the member. |
| `firstName` | string | no | First name displayed on the business card. |
| `lastName` | string | no | Last name displayed on the business card. |
| `phone` | string | no | Phone number displayed on the business card. |
| `function` | string | no | Position displayed on the business card. |
| `information` | string | no | Additional information displayed on the business card. |
| `trivia` | string | no | Mood or status displayed on the business card. |
| `address` | string | no | Address displayed on the business card. |
| `token` | string | no | Optional explicit member token. |
| `tags[]` | array<string> | no | List of tags associated with the member. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "banned": true,
      "created_at": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "information": "string",
      "job_title": "string",
      "last_name": "Chen",
      "name": "Ava Chen",
      "phone": "string",
      "room_private_access_links": [
        {}
      ],
      "tags": [
        "string"
      ],
      "token": "string",
      "trivia": "string",
      "updated_at": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `banned` | boolean |  |
| `created_at` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `information` | string |  |
| `job_title` | string |  |
| `last_name` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `room_private_access_links` | array<object> |  |
| `tags` | array<string> |  |
| `token` | string |  |
| `trivia` | string |  |
| `updated_at` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native WorkAdventure API, this operation is `POST /api/v1/worlds/:worldSlug/members` (base URL `https://admin.workadventu.re`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-member.md) for the provider-specific parameters and requirements.

