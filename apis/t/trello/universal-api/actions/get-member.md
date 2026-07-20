# Trello: Get Member

Retrieves a member from Trello.

```
GET https://connect.mindcloud.co/v1/universal/trello/latest/actions/get-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trello `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Default: `me`. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aaBlockSyncUntil` | object |  |
| `aaEmail` | object |  |
| `aaEnrolledDate` | object |  |
| `aaId` | string |  |
| `activityBlocked` | boolean |  |
| `avatarHash` | string |  |
| `avatarSource` | string |  |
| `avatarUrl` | string |  |
| `bio` | string |  |
| `bioData` | object |  |
| `confirmed` | boolean |  |
| `credentialsRemovedCount` | number |  |
| `dateLastActive` | string |  |
| `dateLastImpression` | string |  |
| `domainClaimed` | object |  |
| `email` | string |  |
| `fullName` | string |  |
| `gravatarHash` | string |  |
| `id` | string |  |
| `idBoards[]` | string |  |
| `idEnterprise` | object |  |
| `idMemberReferrer` | string |  |
| `idOrganizations[]` | string |  |
| `initials` | string |  |
| `isAaMastered` | boolean |  |
| `ixUpdate` | string |  |
| `limits.boards.totalPerMember.disableAt` | number |  |
| `limits.boards.totalPerMember.status` | string |  |
| `limits.boards.totalPerMember.warnAt` | number |  |
| `limits.orgs.totalPerMember.disableAt` | number |  |
| `limits.orgs.totalPerMember.status` | string |  |
| `limits.orgs.totalPerMember.warnAt` | number |  |
| `loginTypes[]` | string |  |
| `marketingOptIn.date` | string |  |
| `marketingOptIn.optedIn` | boolean |  |
| `memberType` | string |  |
| `nodeId` | string |  |
| `nonPublicAvailable` | boolean |  |
| `oneTimeMessagesDismissed[]` | string |  |
| `prefs.colorBlind` | boolean |  |
| `prefs.keyboardShortcutsEnabled` | boolean |  |
| `prefs.locale` | string |  |
| `prefs.minutesBeforeDeadlineToNotify` | number |  |
| `prefs.minutesBetweenSummaries` | number |  |
| `prefs.privacy.avatar` | string |  |
| `prefs.privacy.fullName` | string |  |
| `prefs.sendSummaries` | boolean |  |
| `sessionType` | object |  |
| `status` | string |  |
| `uploadedAvatarHash` | object |  |
| `uploadedAvatarUrl` | object |  |
| `url` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Trello API, this operation is `GET members/:id` (base URL `https://api.trello.com/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-member.md) for the provider-specific parameters and requirements.

