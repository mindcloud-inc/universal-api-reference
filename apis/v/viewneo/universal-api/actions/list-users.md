# Viewneo: List Users

Retrieves users for the current account in Viewneo.

```
GET https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewneo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/list-users?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": 1,
      "createdAt": "string",
      "deletedAt": {},
      "displayLanguage": "string",
      "email": "ava@example.com",
      "emailChangeRequestedAt": {},
      "emailToChange": {},
      "errorCounter": 1,
      "fax": {},
      "firstname": "Ava",
      "id": 1,
      "isAffiliateEmail": 1,
      "isBlocked": 1,
      "isNewsletterSubscribed": 1,
      "lastLoginAttemptAt": {},
      "lastname": "Chen",
      "loggedInAt": "string",
      "mobile": {},
      "phone": {},
      "qrToken": {},
      "salutation": "string",
      "tfaActivatedAt": {},
      "tfaEmail": {},
      "tfaSecretKey": {},
      "updatedAt": "string",
      "userGroup": {
        "companyId": {},
        "createdAt": "string",
        "deletedAt": {},
        "description": {},
        "id": 1,
        "name": "Ava Chen",
        "pivot": {
          "userGroupId": 1,
          "userId": 1
        },
        "type": 1,
        "updatedAt": "string"
      },
      "userGroupId": 1,
      "userGroups": [
        {
          "companyId": {},
          "createdAt": "string",
          "deletedAt": {},
          "description": {},
          "id": 1,
          "name": "Ava Chen",
          "permittedFeatures": [
            {
              "action": "string",
              "companyId": {},
              "createdAt": "string",
              "deletedAt": {},
              "id": 1,
              "isPermitted": 1,
              "resourceId": {},
              "resourceType": "string",
              "scopeId": {},
              "scopeType": {},
              "senderId": {},
              "updatedAt": "string",
              "userGroupId": 1,
              "userId": {}
            }
          ],
          "pivot": {
            "userGroupId": 1,
            "userId": 1
          },
          "type": 1,
          "updatedAt": "string"
        }
      ],
      "verifiedAt": "string",
      "zohoCrmContactId": {},
      "zohoCrmLeadId": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | number |  |
| `createdAt` | string |  |
| `deletedAt` | object |  |
| `displayLanguage` | string |  |
| `email` | string |  |
| `emailChangeRequestedAt` | object |  |
| `emailToChange` | object |  |
| `errorCounter` | number |  |
| `fax` | object |  |
| `firstname` | string |  |
| `id` | number |  |
| `isAffiliateEmail` | number |  |
| `isBlocked` | number |  |
| `isNewsletterSubscribed` | number |  |
| `lastLoginAttemptAt` | object |  |
| `lastname` | string |  |
| `loggedInAt` | string |  |
| `mobile` | object |  |
| `phone` | object |  |
| `qrToken` | object |  |
| `salutation` | string |  |
| `tfaActivatedAt` | object |  |
| `tfaEmail` | object |  |
| `tfaSecretKey` | object |  |
| `updatedAt` | string |  |
| `userGroup.companyId` | object |  |
| `userGroup.createdAt` | string |  |
| `userGroup.deletedAt` | object |  |
| `userGroup.description` | object |  |
| `userGroup.id` | number |  |
| `userGroup.name` | string |  |
| `userGroup.pivot.userGroupId` | number |  |
| `userGroup.pivot.userId` | number |  |
| `userGroup.type` | number |  |
| `userGroup.updatedAt` | string |  |
| `userGroupId` | number |  |
| `userGroups[].companyId` | object |  |
| `userGroups[].createdAt` | string |  |
| `userGroups[].deletedAt` | object |  |
| `userGroups[].description` | object |  |
| `userGroups[].id` | number |  |
| `userGroups[].name` | string |  |
| `userGroups[].permittedFeatures[].action` | string |  |
| `userGroups[].permittedFeatures[].companyId` | object |  |
| `userGroups[].permittedFeatures[].createdAt` | string |  |
| `userGroups[].permittedFeatures[].deletedAt` | object |  |
| `userGroups[].permittedFeatures[].id` | number |  |
| `userGroups[].permittedFeatures[].isPermitted` | number |  |
| `userGroups[].permittedFeatures[].resourceId` | object |  |
| `userGroups[].permittedFeatures[].resourceType` | string |  |
| `userGroups[].permittedFeatures[].scopeId` | object |  |
| `userGroups[].permittedFeatures[].scopeType` | object |  |
| `userGroups[].permittedFeatures[].senderId` | object |  |
| `userGroups[].permittedFeatures[].updatedAt` | string |  |
| `userGroups[].permittedFeatures[].userGroupId` | number |  |
| `userGroups[].permittedFeatures[].userId` | object |  |
| `userGroups[].pivot.userGroupId` | number |  |
| `userGroups[].pivot.userId` | number |  |
| `userGroups[].type` | number |  |
| `userGroups[].updatedAt` | string |  |
| `verifiedAt` | string |  |
| `zohoCrmContactId` | object |  |
| `zohoCrmLeadId` | object |  |

## Native endpoint

Through the native Viewneo API, this operation is `GET /user` (base URL `https://cloud.viewneo.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

