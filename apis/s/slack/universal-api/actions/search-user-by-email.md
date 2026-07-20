# Slack: Search User By Email

Finds a Slack user by email address.

```
GET https://connect.mindcloud.co/v1/universal/slack/latest/actions/search-user-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/slack/latest/actions/search-user-by-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/slack/latest/actions/search-user-by-email?${params}`, {
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
| `email` | string | yes | An email address belonging to a user in the workspace |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "deleted": true,
      "has2fa": true,
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
        "avatarHash": "string",
        "displayName": "Ava Chen",
        "displayNameNormalized": "Ava Chen",
        "email": "ava@example.com",
        "image192": "string",
        "image24": "string",
        "image32": "string",
        "image48": "string",
        "image512": "string",
        "image72": "string",
        "phone": "string",
        "realName": "Ava Chen",
        "realNameNormalized": "Ava Chen",
        "skype": "string",
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
      "updated": 1,
      "whoCanShareContactCard": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `deleted` | boolean |  |
| `has2fa` | boolean |  |
| `id` | string |  |
| `isAdmin` | boolean |  |
| `isAppUser` | boolean |  |
| `isBot` | boolean |  |
| `isEmailConfirmed` | boolean |  |
| `isOwner` | boolean |  |
| `isPrimaryOwner` | boolean |  |
| `isRestricted` | boolean |  |
| `isUltraRestricted` | boolean |  |
| `name` | string |  |
| `profile.avatarHash` | string |  |
| `profile.displayName` | string |  |
| `profile.displayNameNormalized` | string |  |
| `profile.email` | string |  |
| `profile.image192` | string |  |
| `profile.image24` | string |  |
| `profile.image32` | string |  |
| `profile.image48` | string |  |
| `profile.image512` | string |  |
| `profile.image72` | string |  |
| `profile.phone` | string |  |
| `profile.realName` | string |  |
| `profile.realNameNormalized` | string |  |
| `profile.skype` | string |  |
| `profile.statusEmoji` | string |  |
| `profile.statusExpiration` | number |  |
| `profile.statusText` | string |  |
| `profile.statusTextCanonical` | string |  |
| `profile.team` | string |  |
| `profile.title` | string |  |
| `realName` | string |  |
| `teamId` | string |  |
| `tz` | string |  |
| `tzLabel` | string |  |
| `tzOffset` | number |  |
| `updated` | number |  |
| `whoCanShareContactCard` | string |  |

## Native endpoint

Through the native Slack API, this operation is `GET users.lookupByEmail` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-user-by-email.md) for the provider-specific parameters and requirements.

