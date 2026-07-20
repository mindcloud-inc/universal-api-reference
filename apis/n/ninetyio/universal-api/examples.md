# Ninety.io Universal API Examples

These examples use the MindCloud API key and Ninety.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Teams

Retrieves teams from Ninety.io.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/get-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/get-teams?${params}`, {
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
      "_id": "string",
      "companyId": "string",
      "deleted": true,
      "name": "Ava Chen",
      "project": true
    }
  ],
  "meta": {}
}
```

See the full [Get Teams action reference](actions/get-teams.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ninetyio/latest/actions/get-teams).

## Create Issue

Creates a new issue in Ninety.io.

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

Example response:

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

See the full [Create Issue action reference](actions/create-issue.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ninetyio/latest/actions/create-issue).
