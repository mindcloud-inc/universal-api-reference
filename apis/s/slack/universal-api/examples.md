# Slack Universal API Examples

These examples use the MindCloud API key and Slack connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves users from a Slack workspace.

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

Example response:

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

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/slack/latest/actions/list-users).

## Add Reaction

Adds a reaction to an item in Slack.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/slack/latest/actions/add-reaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channel": "string",
  "timestamp": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/slack/latest/actions/add-reaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channel": "string",
    "timestamp": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add Reaction action reference](actions/add-reaction.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/slack/latest/actions/add-reaction).
