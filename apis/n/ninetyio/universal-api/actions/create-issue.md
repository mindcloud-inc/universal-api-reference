# Ninety.io: Create Issue

Creates a new issue in Ninety.io.

```
POST https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/create-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninety.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/create-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "teamId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/create-issue', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "teamId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes |  |
| `teamId` | string | yes |  |
| `interval` | string | no | Issue classification |
| `description` | string | no | HTML description of the Issue |
| `priority` | number | no | Priority level from 0 (none) to 5 (highest) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "archivedDate": {},
      "companyId": "string",
      "completed": true,
      "completedDate": {},
      "createdBy": "string",
      "createdByUserId": "string",
      "createdDate": "string",
      "deleted": true,
      "deletedDate": {},
      "description": "string",
      "followers": [
        "string"
      ],
      "Id": "string",
      "imported": true,
      "intervalCode": "string",
      "numOfLikes": 1,
      "ordinal": 1,
      "planningBoardOrdinal": 1,
      "rating": {},
      "teamId": "string",
      "title": "string",
      "user": {
        "active": true,
        "createdAt": {},
        "deleted": true,
        "freePlanNotificationDismissed": {},
        "guideDismissed": {},
        "guideEnabled": true,
        "guideViewed": true,
        "hasRubiconAccess": {},
        "howCanWeHelpList": [
          "string"
        ],
        "Id": "string",
        "inviteFailed": {},
        "isHelpful": true,
        "isImplementer": {},
        "lastOpenedNotificationFeedAt": {},
        "liteMeasurables": {},
        "localMetadata": {},
        "managerPermissionChangesNotificationDismissed": {},
        "metadata": {
          "deleted": true,
          "Id": "string",
          "name": {
            "first": "Ava Chen",
            "last": "Ava Chen"
          },
          "picture": {}
        },
        "pageViews": {
          "userSettings": 1
        },
        "personId": "string",
        "personMetadataId": "string",
        "preImplementer": {},
        "primaryEmail": {},
        "renewalNotificationDismissedKey": {},
        "roleCode": "string",
        "shouldInvite": {},
        "signupCompanyRole": "string",
        "status": {},
        "tutorialsHidden": {},
        "updatedSubscriptionDismissed": {},
        "V": 1
      },
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `archivedDate` | object |  |
| `companyId` | string |  |
| `completed` | boolean |  |
| `completedDate` | object |  |
| `createdBy` | string |  |
| `createdByUserId` | string |  |
| `createdDate` | string |  |
| `deleted` | boolean |  |
| `deletedDate` | object |  |
| `description` | string |  |
| `followers[]` | string |  |
| `Id` | string |  |
| `imported` | boolean |  |
| `intervalCode` | string |  |
| `numOfLikes` | number |  |
| `ordinal` | number |  |
| `planningBoardOrdinal` | number |  |
| `rating` | object |  |
| `teamId` | string |  |
| `title` | string |  |
| `user.active` | boolean |  |
| `user.createdAt` | object |  |
| `user.deleted` | boolean |  |
| `user.freePlanNotificationDismissed` | object |  |
| `user.guideDismissed` | object |  |
| `user.guideEnabled` | boolean |  |
| `user.guideViewed` | boolean |  |
| `user.hasRubiconAccess` | object |  |
| `user.howCanWeHelpList[]` | string |  |
| `user.Id` | string |  |
| `user.inviteFailed` | object |  |
| `user.isHelpful` | boolean |  |
| `user.isImplementer` | object |  |
| `user.lastOpenedNotificationFeedAt` | object |  |
| `user.liteMeasurables` | object |  |
| `user.localMetadata` | object |  |
| `user.managerPermissionChangesNotificationDismissed` | object |  |
| `user.metadata.deleted` | boolean |  |
| `user.metadata.Id` | string |  |
| `user.metadata.name.first` | string |  |
| `user.metadata.name.last` | string |  |
| `user.metadata.picture` | object |  |
| `user.pageViews.userSettings` | number |  |
| `user.personId` | string |  |
| `user.personMetadataId` | string |  |
| `user.preImplementer` | object |  |
| `user.primaryEmail` | object |  |
| `user.renewalNotificationDismissedKey` | object |  |
| `user.roleCode` | string |  |
| `user.shouldInvite` | object |  |
| `user.signupCompanyRole` | string |  |
| `user.status` | object |  |
| `user.tutorialsHidden` | object |  |
| `user.updatedSubscriptionDismissed` | object |  |
| `user.V` | number |  |
| `userId` | string |  |

## Native endpoint

Through the native Ninety.io API, this operation is `POST /v1/issues` (base URL `https://api.public.ninety.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-issue.md) for the provider-specific parameters and requirements.

