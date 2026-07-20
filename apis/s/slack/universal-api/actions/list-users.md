# Slack: List Users

Retrieves users from a Slack workspace.

```
GET https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-users?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeLocale` | boolean | no | Set this to true to receive the locale for users. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "deleted": true,
      "id": "string",
      "isAdmin": true,
      "isAppUser": true,
      "isBot": true,
      "isEmailConfirmed": true,
      "isOwner": true,
      "isPrimaryOwner": true,
      "isRestricted": true,
      "isUltraRestricted": true,
      "name": "Ava Chen",
      "profile": {
        "alwaysActive": true,
        "avatarHash": "string",
        "displayName": "Ava Chen",
        "displayNameNormalized": "Ava Chen",
        "email": "ava@example.com",
        "firstName": "Ava",
        "image192": "string",
        "image24": "string",
        "image32": "string",
        "image48": "string",
        "image512": "string",
        "image72": "string",
        "lastName": "Chen",
        "phone": "string",
        "realName": "Ava Chen",
        "realNameNormalized": "Ava Chen",
        "skype": "Ava Chen",
        "statusEmoji": "string",
        "statusExpiration": 1,
        "statusText": "string",
        "statusTextCanonical": "string",
        "team": "string",
        "title": "string"
      },
      "realName": "Ava Chen",
      "teamId": "string",
      "tz": "string",
      "tzLabel": "string",
      "tzOffset": 1,
      "updated": "2026-05-07T12:00:00.000Z",
      "whoCanShareContactCard": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string | The color of the user. |
| `deleted` | boolean | Whether or not the user has been deleted. |
| `id` | string | The unique identifier for the user. |
| `isAdmin` | boolean | Whether or not the user is an admin. |
| `isAppUser` | boolean | Whether or not the user is an app user. |
| `isBot` | boolean | Whether or not the user is a bot. |
| `isEmailConfirmed` | boolean | Whether or not the user's email is confirmed. |
| `isOwner` | boolean | Whether or not the user is an owner. |
| `isPrimaryOwner` | boolean | Whether or not the user is a primary owner. |
| `isRestricted` | boolean | Whether or not the user is restricted. |
| `isUltraRestricted` | boolean | Whether or not the user is ultra restricted. |
| `name` | string | The username of the user. |
| `profile` | object |  |
| `profile.alwaysActive` | boolean | Whether or not the user's profile is always active. |
| `profile.avatarHash` | string | The avatar hash of the user's profile. |
| `profile.displayName` | string | The display name of the user's profile. |
| `profile.displayNameNormalized` | string | The normalized display name of the user's profile. |
| `profile.email` | string |  |
| `profile.firstName` | string | The first name of the user's profile. |
| `profile.image192` | string | The 192x192 image of the user's profile. |
| `profile.image24` | string | The 24x24 image of the user's profile. |
| `profile.image32` | string | The 32x32 image of the user's profile. |
| `profile.image48` | string | The 48x48 image of the user's profile. |
| `profile.image512` | string | The 512x512 image of the user's profile. |
| `profile.image72` | string | The 72x72 image of the user's profile. |
| `profile.lastName` | string | The last name of the user's profile. |
| `profile.phone` | string | The phone number of the user's profile. |
| `profile.realName` | string | The real name of the user's profile. |
| `profile.realNameNormalized` | string | The normalized real name of the user's profile. |
| `profile.skype` | string | The Skype username of the user's profile. |
| `profile.statusEmoji` | string | The status emoji of the user's profile. |
| `profile.statusExpiration` | number | The status expiration of the user's profile. |
| `profile.statusText` | string | The status text of the user's profile. |
| `profile.statusTextCanonical` | string | The canonical status text of the user's profile. |
| `profile.team` | string | The team of the user's profile. |
| `profile.title` | string | The title of the user's profile. |
| `realName` | string | The real name of the user. |
| `teamId` | string | The unique identifier for the team. |
| `tz` | string | The time zone of the user. |
| `tzLabel` | string | The label for the user's time zone. |
| `tzOffset` | number | The offset for the user's time zone. |
| `updated` | date | The timestamp for when the user was last updated. |
| `whoCanShareContactCard` | string | Who can share the user's contact card. |

## Native endpoint

Through the native Slack API, this operation is `GET users.list` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

