# Productive.io: List People

Retrieves people from your Productive.io account.

```
GET https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productive.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-people?${params}`, {
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
      "attributes": {
        "agent": true,
        "archivedAt": "string",
        "autotracking": true,
        "availabilities": "string",
        "avatarUrl": "https://example.com",
        "champion": true,
        "colorId": "string",
        "createdAt": "string",
        "customFields": "string",
        "deactivatedAt": "string",
        "email": "ava@example.com",
        "externalId": "string",
        "externalSync": true,
        "firstName": "Ava",
        "hrmTypeId": 1,
        "invitedAt": "string",
        "isUser": true,
        "joinedAt": "string",
        "lastActivityAt": "string",
        "lastName": "Chen",
        "lastSeenAt": "string",
        "nickname": "Ava Chen",
        "offboardingId": "string",
        "offboardingStatus": "string",
        "originalAvatarUrl": "https://example.com",
        "placeholder": true,
        "roleId": 1,
        "sampleData": true,
        "statusEmoji": "string",
        "statusExpiresAt": "string",
        "statusText": "string",
        "tagList": [
          "string"
        ],
        "timeOffStatusSync": true,
        "timesheetSubmissionDisabled": true,
        "timeTrackingPolicyId": "string",
        "timeUnlocked": true,
        "timeUnlockedEndDate": "string",
        "timeUnlockedInterval": "string",
        "timeUnlockedOn": "string",
        "timeUnlockedPeriodId": "string",
        "timeUnlockedStartDate": "string",
        "title": "string",
        "twoFactorAuth": true,
        "userId": 1,
        "virtual": true
      },
      "id": "string",
      "relationships": {
        "approvalPolicyAssignment": {
          "meta": {
            "included": true
          }
        },
        "company": {
          "meta": {
            "included": true
          }
        },
        "customFieldAttachments": {
          "meta": {
            "included": true
          }
        },
        "customFieldPeople": {
          "meta": {
            "included": true
          }
        },
        "customRole": {
          "meta": {
            "included": true
          }
        },
        "manager": {
          "meta": {
            "included": true
          }
        },
        "organization": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "serviceTypes": {
          "meta": {
            "included": true
          }
        },
        "subsidiary": {
          "meta": {
            "included": true
          }
        },
        "teams": {
          "meta": {
            "included": true
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.agent` | boolean |  |
| `attributes.archivedAt` | string |  |
| `attributes.autotracking` | boolean |  |
| `attributes.availabilities` | string |  |
| `attributes.avatarUrl` | string |  |
| `attributes.champion` | boolean |  |
| `attributes.colorId` | string |  |
| `attributes.createdAt` | string |  |
| `attributes.customFields` | string |  |
| `attributes.deactivatedAt` | string |  |
| `attributes.email` | string |  |
| `attributes.externalId` | string |  |
| `attributes.externalSync` | boolean |  |
| `attributes.firstName` | string |  |
| `attributes.hrmTypeId` | number |  |
| `attributes.invitedAt` | string |  |
| `attributes.isUser` | boolean |  |
| `attributes.joinedAt` | string |  |
| `attributes.lastActivityAt` | string |  |
| `attributes.lastName` | string |  |
| `attributes.lastSeenAt` | string |  |
| `attributes.nickname` | string |  |
| `attributes.offboardingId` | string |  |
| `attributes.offboardingStatus` | string |  |
| `attributes.originalAvatarUrl` | string |  |
| `attributes.placeholder` | boolean |  |
| `attributes.roleId` | number |  |
| `attributes.sampleData` | boolean |  |
| `attributes.statusEmoji` | string |  |
| `attributes.statusExpiresAt` | string |  |
| `attributes.statusText` | string |  |
| `attributes.tagList` | array<string> |  |
| `attributes.timeOffStatusSync` | boolean |  |
| `attributes.timesheetSubmissionDisabled` | boolean |  |
| `attributes.timeTrackingPolicyId` | string |  |
| `attributes.timeUnlocked` | boolean |  |
| `attributes.timeUnlockedEndDate` | string |  |
| `attributes.timeUnlockedInterval` | string |  |
| `attributes.timeUnlockedOn` | string |  |
| `attributes.timeUnlockedPeriodId` | string |  |
| `attributes.timeUnlockedStartDate` | string |  |
| `attributes.title` | string |  |
| `attributes.twoFactorAuth` | boolean |  |
| `attributes.userId` | number |  |
| `attributes.virtual` | boolean |  |
| `id` | string |  |
| `relationships.approvalPolicyAssignment.meta.included` | boolean |  |
| `relationships.company.meta.included` | boolean |  |
| `relationships.customFieldAttachments.meta.included` | boolean |  |
| `relationships.customFieldPeople.meta.included` | boolean |  |
| `relationships.customRole.meta.included` | boolean |  |
| `relationships.manager.meta.included` | boolean |  |
| `relationships.organization.data.id` | string |  |
| `relationships.organization.data.type` | string |  |
| `relationships.serviceTypes.meta.included` | boolean |  |
| `relationships.subsidiary.meta.included` | boolean |  |
| `relationships.teams.meta.included` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Productive.io API, this operation is `GET /people` (base URL `https://api.productive.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-people.md) for the provider-specific parameters and requirements.

