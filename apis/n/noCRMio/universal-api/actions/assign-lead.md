# noCRM.io: Assign Lead

Assigns a lead in noCRM.io.

```
PUT https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/assign-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a noCRM.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/assign-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/assign-lead', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The identifier of the lead. |
| `userId` | string | yes | User ID or email to assign the lead to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": {},
      "amountPercentage": {},
      "attachmentCount": 1,
      "clientFolderId": {},
      "clientFolderName": {},
      "closedAt": {},
      "commentCount": 1,
      "createdAt": "string",
      "createdById": 1,
      "createdFrom": "string",
      "currency": {},
      "description": "string",
      "estimatedClosingDate": {},
      "extendedInfo": {
        "allContactEmails": [
          [
            "ava@example.com"
          ]
        ],
        "allPhonesWithNameAndType": [
          [
            "Ava Chen"
          ]
        ],
        "attachments": [
          [
            "string"
          ]
        ],
        "bccCount": 1,
        "businessCardId": {},
        "clientFolder": {},
        "commentCount": 1,
        "createdBy": {
          "email": "ava@example.com",
          "firstname": "Ava",
          "id": 1,
          "lastname": "Chen",
          "mobilePhone": {},
          "phone": {}
        },
        "fields": {
          "address": {},
          "city": {},
          "companyId": {},
          "country": {},
          "custom1": {},
          "custom2": {},
          "custom3": {},
          "custom4": {},
          "custom5": {},
          "email": {},
          "fax": {},
          "firstName": {},
          "fullName": {},
          "job": {},
          "lastName": {},
          "mobile": {},
          "phone": {},
          "state": {},
          "vat": {},
          "web": {},
          "zipcode": {}
        },
        "fieldsByName": {
          "email": {},
          "firstName": {},
          "lastName": {},
          "phone": {}
        },
        "firstContactEmail": {},
        "followUps": [
          [
            "string"
          ]
        ],
        "permalink": "https://example.com",
        "team": {},
        "user": {
          "email": "ava@example.com",
          "firstname": "Ava",
          "id": 1,
          "lastname": "Chen",
          "mobilePhone": {},
          "phone": {}
        },
        "visibleByCount": 1
      },
      "htmlDescription": "string",
      "id": 1,
      "nextActionAt": "string",
      "pipeline": "string",
      "probability": {},
      "probabilizedAmount": 1,
      "remindDate": "string",
      "reminderActivityId": {},
      "reminderActivityLogId": {},
      "reminderAt": {},
      "reminderDuration": {},
      "reminderNote": {},
      "remindTime": {},
      "secondNumber": {},
      "starred": true,
      "status": "string",
      "step": "string",
      "stepId": 1,
      "tags": [
        [
          "string"
        ]
      ],
      "teamId": {},
      "title": "string",
      "updatedAt": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | object |  |
| `amountPercentage` | object |  |
| `attachmentCount` | number |  |
| `clientFolderId` | object |  |
| `clientFolderName` | object |  |
| `closedAt` | object |  |
| `commentCount` | number |  |
| `createdAt` | string |  |
| `createdById` | number |  |
| `createdFrom` | string |  |
| `currency` | object |  |
| `description` | string |  |
| `estimatedClosingDate` | object |  |
| `extendedInfo` | object |  |
| `extendedInfo.allContactEmails[]` | array<string> |  |
| `extendedInfo.allPhonesWithNameAndType[]` | array<string> |  |
| `extendedInfo.attachments[]` | array<string> |  |
| `extendedInfo.bccCount` | number |  |
| `extendedInfo.businessCardId` | object |  |
| `extendedInfo.clientFolder` | object |  |
| `extendedInfo.commentCount` | number |  |
| `extendedInfo.createdBy` | object |  |
| `extendedInfo.createdBy.email` | string |  |
| `extendedInfo.createdBy.firstname` | string |  |
| `extendedInfo.createdBy.id` | number |  |
| `extendedInfo.createdBy.lastname` | string |  |
| `extendedInfo.createdBy.mobilePhone` | object |  |
| `extendedInfo.createdBy.phone` | object |  |
| `extendedInfo.fields` | object |  |
| `extendedInfo.fields.address` | object |  |
| `extendedInfo.fields.city` | object |  |
| `extendedInfo.fields.companyId` | object |  |
| `extendedInfo.fields.country` | object |  |
| `extendedInfo.fields.custom1` | object |  |
| `extendedInfo.fields.custom2` | object |  |
| `extendedInfo.fields.custom3` | object |  |
| `extendedInfo.fields.custom4` | object |  |
| `extendedInfo.fields.custom5` | object |  |
| `extendedInfo.fields.email` | object |  |
| `extendedInfo.fields.fax` | object |  |
| `extendedInfo.fields.firstName` | object |  |
| `extendedInfo.fields.fullName` | object |  |
| `extendedInfo.fields.job` | object |  |
| `extendedInfo.fields.lastName` | object |  |
| `extendedInfo.fields.mobile` | object |  |
| `extendedInfo.fields.phone` | object |  |
| `extendedInfo.fields.state` | object |  |
| `extendedInfo.fields.vat` | object |  |
| `extendedInfo.fields.web` | object |  |
| `extendedInfo.fields.zipcode` | object |  |
| `extendedInfo.fieldsByName` | object |  |
| `extendedInfo.fieldsByName.email` | object |  |
| `extendedInfo.fieldsByName.firstName` | object |  |
| `extendedInfo.fieldsByName.lastName` | object |  |
| `extendedInfo.fieldsByName.phone` | object |  |
| `extendedInfo.firstContactEmail` | object |  |
| `extendedInfo.followUps[]` | array<string> |  |
| `extendedInfo.permalink` | string |  |
| `extendedInfo.team` | object |  |
| `extendedInfo.user` | object |  |
| `extendedInfo.user.email` | string |  |
| `extendedInfo.user.firstname` | string |  |
| `extendedInfo.user.id` | number |  |
| `extendedInfo.user.lastname` | string |  |
| `extendedInfo.user.mobilePhone` | object |  |
| `extendedInfo.user.phone` | object |  |
| `extendedInfo.visibleByCount` | number |  |
| `htmlDescription` | string |  |
| `id` | number |  |
| `nextActionAt` | string |  |
| `pipeline` | string |  |
| `probability` | object |  |
| `probabilizedAmount` | number |  |
| `remindDate` | string |  |
| `reminderActivityId` | object |  |
| `reminderActivityLogId` | object |  |
| `reminderAt` | object |  |
| `reminderDuration` | object |  |
| `reminderNote` | object |  |
| `remindTime` | object |  |
| `secondNumber` | object |  |
| `starred` | boolean |  |
| `status` | string |  |
| `step` | string |  |
| `stepId` | number |  |
| `tags[]` | array<string> |  |
| `teamId` | object |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native noCRM.io API, this operation is `POST /leads/:id/assign` (base URL `{{credentials.baseUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-lead.md) for the provider-specific parameters and requirements.

