# Clockify: Update Member Profile

Updates a member profile in Clockify.

```
PUT https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-member-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-member-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "userId": "string",
  "userCustomFields[].customFieldId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-member-profile', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "userId": "string",
    "userCustomFields[].customFieldId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `userId` | string<string> | yes |  |
| `imageUrl` | string | no | Example: `https://example.com/webhook`. |
| `name` | string | no | Example: `Example Name`. |
| `removeProfileImage` | boolean | no | Example: `true`. |
| `userCustomFields[]` | array<object> | no |  |
| `weekStart` | list<string> | no | One of: `FRIDAY`, `MONDAY`, `SATURDAY`, `SUNDAY`, `THURSDAY`, `TUESDAY`, `WEDNESDAY`. Example: `2026-01-01`. |
| `workCapacity` | string | no |  |
| `workingDays` | list<string> | no | One of: `FRIDAY`, `MONDAY`, `SATURDAY`, `SUNDAY`, `THURSDAY`, `TUESDAY`, `WEDNESDAY`. |
| `userCustomFields[].customFieldId` | string | yes |  |
| `userCustomFields[].value` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "hasPassword": true,
      "hasPendingApprovalRequest": true,
      "imageUrl": "https://example.com",
      "name": "Ava Chen",
      "userCustomFieldValues": [
        [
          {}
        ]
      ],
      "weekStart": "string",
      "workCapacity": "string",
      "workingDays": "string",
      "workspaceNumber": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `hasPassword` | boolean |  |
| `hasPendingApprovalRequest` | boolean |  |
| `imageUrl` | string |  |
| `name` | string |  |
| `userCustomFieldValues[]` | array<object> |  |
| `userCustomFieldValues[].customField` | object |  |
| `userCustomFieldValues[].customField.allowedValues[]` | array<string> |  |
| `userCustomFieldValues[].customField.description` | string |  |
| `userCustomFieldValues[].customField.entityType` | string |  |
| `userCustomFieldValues[].customField.id` | string |  |
| `userCustomFieldValues[].customField.name` | string |  |
| `userCustomFieldValues[].customField.onlyAdminCanEdit` | boolean |  |
| `userCustomFieldValues[].customField.placeholder` | string |  |
| `userCustomFieldValues[].customField.projectDefaultValues[]` | array<object> |  |
| `userCustomFieldValues[].customField.projectDefaultValues[].projectId` | string |  |
| `userCustomFieldValues[].customField.projectDefaultValues[].status` | string |  |
| `userCustomFieldValues[].customField.projectDefaultValues[].value` | object |  |
| `userCustomFieldValues[].customField.required` | boolean |  |
| `userCustomFieldValues[].customField.status` | string |  |
| `userCustomFieldValues[].customField.type` | string |  |
| `userCustomFieldValues[].customField.workspaceDefaultValue` | object |  |
| `userCustomFieldValues[].customField.workspaceId` | string |  |
| `userCustomFieldValues[].customFieldId` | string |  |
| `userCustomFieldValues[].name` | string |  |
| `userCustomFieldValues[].sourceType` | string |  |
| `userCustomFieldValues[].type` | string |  |
| `userCustomFieldValues[].userId` | string |  |
| `userCustomFieldValues[].value` | object |  |
| `weekStart` | string |  |
| `workCapacity` | string |  |
| `workingDays` | string |  |
| `workspaceNumber` | number |  |

## Native endpoint

Through the native Clockify API, this operation is `PATCH workspaces/:workspaceId/member-profile/:userId` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-member-profile.md) for the provider-specific parameters and requirements.

