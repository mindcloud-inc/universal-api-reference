# Slack: Get User Information

Retrieves user details from a Slack workspace.

```
GET https://connect.mindcloud.co/v1/universal/slack/latest/actions/get-user-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/slack/latest/actions/get-user-information?connectionId=$CONNECTION_ID&user=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "user": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/slack/latest/actions/get-user-information?${params}`, {
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
| `user` | list | yes | User to get info on |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeLocale` | boolean | no | Set this to true to receive the locale for this user. Defaults to false |

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

Through the native Slack API, this operation is `GET users.info` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-information.md) for the provider-specific parameters and requirements.

