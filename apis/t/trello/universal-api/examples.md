# Trello Universal API Examples

These examples use the MindCloud API key and Trello connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Member

Retrieves a member from Trello.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trello/latest/actions/get-member?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trello/latest/actions/get-member?${params}`, {
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
      "aaBlockSyncUntil": {},
      "aaEmail": {},
      "aaEnrolledDate": {},
      "aaId": "string",
      "activityBlocked": true,
      "avatarHash": "string",
      "avatarSource": "string",
      "avatarUrl": "https://example.com",
      "bio": "string",
      "bioData": {},
      "confirmed": true,
      "credentialsRemovedCount": 1,
      "dateLastActive": "string",
      "dateLastImpression": "string",
      "domainClaimed": {},
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "gravatarHash": "string",
      "id": "string",
      "idBoards": [
        "string"
      ],
      "idEnterprise": {},
      "idMemberReferrer": "string",
      "idOrganizations": [
        "string"
      ],
      "initials": "string",
      "isAaMastered": true,
      "ixUpdate": "string",
      "limits": {
        "boards": {
          "totalPerMember": {
            "disableAt": 1,
            "status": "string",
            "warnAt": 1
          }
        },
        "orgs": {
          "totalPerMember": {
            "disableAt": 1,
            "status": "string",
            "warnAt": 1
          }
        }
      },
      "loginTypes": [
        "string"
      ],
      "marketingOptIn": {
        "date": "string",
        "optedIn": true
      },
      "memberType": "string",
      "nodeId": "string",
      "nonPublicAvailable": true,
      "oneTimeMessagesDismissed": [
        "string"
      ],
      "prefs": {
        "colorBlind": true,
        "keyboardShortcutsEnabled": true,
        "locale": "string",
        "minutesBeforeDeadlineToNotify": 1,
        "minutesBetweenSummaries": 1,
        "privacy": {
          "avatar": "string",
          "fullName": "Ava Chen"
        },
        "sendSummaries": true
      },
      "sessionType": {},
      "status": "string",
      "uploadedAvatarHash": {},
      "uploadedAvatarUrl": {},
      "url": "https://example.com",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Member action reference](actions/get-member.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trello/latest/actions/get-member).

## Add Attachment to Card

Adds an attachment to a Trello card.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/trello/latest/actions/add-attachment-to-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trello/latest/actions/add-attachment-to-card', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "idMember": "string",
      "name": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Add Attachment to Card action reference](actions/add-attachment-to-card.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trello/latest/actions/add-attachment-to-card).
