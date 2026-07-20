# Ninety.io: Query Issues

Retrieves issues from Ninety.io with optional team and interval filters.

```
GET https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/query-issues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninety.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/query-issues?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/query-issues?${params}`, {
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
| `sortField` | string | no | The field to sort results by |
| `sortDirection` | string | no | The sort direction |
| `pageSize` | number | no | Number of items per page |
| `pageIndex` | number | no | Zero-based page index |
| `teamId` | string | no | A single team Id or a comma-separated list of team Ids to filter by |
| `intervalCode` | string | no | Filter by Issue classification |
| `searchText` | string | no | Search text to match against Issue title, description, and comments |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
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
          "description": "string",
          "followers": [
            "string"
          ],
          "Id": "string",
          "imported": true,
          "intervalCode": "string",
          "numOfLikes": 1,
          "ordinal": 1,
          "originalDueDate": {},
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
      "params": {
        "pageIndex": 1,
        "pageSize": 1,
        "sortDirection": "string",
        "sortField": "string",
        "team": [
          "string"
        ]
      },
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].archived` | boolean |  |
| `items[].archivedDate` | object |  |
| `items[].companyId` | string |  |
| `items[].completed` | boolean |  |
| `items[].completedDate` | object |  |
| `items[].createdBy` | string |  |
| `items[].createdByUserId` | string |  |
| `items[].createdDate` | string |  |
| `items[].deleted` | boolean |  |
| `items[].description` | string |  |
| `items[].followers[]` | string |  |
| `items[].Id` | string |  |
| `items[].imported` | boolean |  |
| `items[].intervalCode` | string |  |
| `items[].numOfLikes` | number |  |
| `items[].ordinal` | number |  |
| `items[].originalDueDate` | object |  |
| `items[].planningBoardOrdinal` | number |  |
| `items[].rating` | object |  |
| `items[].teamId` | string |  |
| `items[].title` | string |  |
| `items[].user.active` | boolean |  |
| `items[].user.createdAt` | object |  |
| `items[].user.deleted` | boolean |  |
| `items[].user.freePlanNotificationDismissed` | object |  |
| `items[].user.guideDismissed` | object |  |
| `items[].user.guideEnabled` | boolean |  |
| `items[].user.guideViewed` | boolean |  |
| `items[].user.hasRubiconAccess` | object |  |
| `items[].user.howCanWeHelpList[]` | string |  |
| `items[].user.Id` | string |  |
| `items[].user.inviteFailed` | object |  |
| `items[].user.isHelpful` | boolean |  |
| `items[].user.isImplementer` | object |  |
| `items[].user.lastOpenedNotificationFeedAt` | object |  |
| `items[].user.liteMeasurables` | object |  |
| `items[].user.localMetadata` | object |  |
| `items[].user.managerPermissionChangesNotificationDismissed` | object |  |
| `items[].user.metadata.deleted` | boolean |  |
| `items[].user.metadata.Id` | string |  |
| `items[].user.metadata.name.first` | string |  |
| `items[].user.metadata.name.last` | string |  |
| `items[].user.metadata.picture` | object |  |
| `items[].user.pageViews.userSettings` | number |  |
| `items[].user.personId` | string |  |
| `items[].user.personMetadataId` | string |  |
| `items[].user.preImplementer` | object |  |
| `items[].user.primaryEmail` | object |  |
| `items[].user.renewalNotificationDismissedKey` | object |  |
| `items[].user.roleCode` | string |  |
| `items[].user.shouldInvite` | object |  |
| `items[].user.signupCompanyRole` | string |  |
| `items[].user.status` | object |  |
| `items[].user.tutorialsHidden` | object |  |
| `items[].user.updatedSubscriptionDismissed` | object |  |
| `items[].user.V` | number |  |
| `items[].userId` | string |  |
| `params.pageIndex` | number |  |
| `params.pageSize` | number |  |
| `params.sortDirection` | string |  |
| `params.sortField` | string |  |
| `params.team[]` | string |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Ninety.io API, this operation is `POST /v1/issues/query` (base URL `https://api.public.ninety.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-issues.md) for the provider-specific parameters and requirements.

