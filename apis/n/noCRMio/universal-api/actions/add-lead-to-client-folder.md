# noCRM.io: Add Lead To Client Folder

Adds a lead to a client folder in noCRM.io.

```
PUT https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/add-lead-to-client-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a noCRM.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/add-lead-to-client-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "clientId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/add-lead-to-client-folder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "clientId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Lead ID. |
| `clientId` | number | yes | Client folder ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "amountPercentage": {},
      "attachmentCount": 1,
      "clientFolderId": 1,
      "clientFolderName": "Ava Chen",
      "closedAt": {},
      "commentCount": 1,
      "createdAt": "string",
      "createdById": 1,
      "createdFrom": "string",
      "currency": "string",
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
        "clientFolder": {
          "createdAt": "string",
          "description": "string",
          "extendedInfo": {
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
              "billingAddress": {},
              "deliveryAddress": {},
              "vATNumber": {}
            },
            "permalink": "https://example.com",
            "user": {
              "email": "ava@example.com",
              "firstname": "Ava",
              "id": 1,
              "lastname": "Chen",
              "mobilePhone": {},
              "phone": {}
            }
          },
          "id": 1,
          "isActive": true,
          "name": "Ava Chen",
          "userId": 1
        },
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
      "probability": 1,
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
| `amount` | number |  |
| `amountPercentage` | object |  |
| `attachmentCount` | number |  |
| `clientFolderId` | number |  |
| `clientFolderName` | string |  |
| `closedAt` | object |  |
| `commentCount` | number |  |
| `createdAt` | string |  |
| `createdById` | number |  |
| `createdFrom` | string |  |
| `currency` | string |  |
| `description` | string |  |
| `estimatedClosingDate` | object |  |
| `extendedInfo` | object |  |
| `extendedInfo.allContactEmails[]` | array<string> |  |
| `extendedInfo.allPhonesWithNameAndType[]` | array<string> |  |
| `extendedInfo.attachments[]` | array<string> |  |
| `extendedInfo.bccCount` | number |  |
| `extendedInfo.businessCardId` | object |  |
| `extendedInfo.clientFolder` | object |  |
| `extendedInfo.clientFolder.createdAt` | string |  |
| `extendedInfo.clientFolder.description` | string |  |
| `extendedInfo.clientFolder.extendedInfo` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fields` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fields.address` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fields.city` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fields.companyId` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fields.country` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fields.custom1` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fields.custom2` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fields.custom3` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fields.custom4` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fields.custom5` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fields.email` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fields.fax` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fields.firstName` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fields.fullName` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fields.job` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fields.lastName` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fields.mobile` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fields.phone` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fields.state` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fields.vat` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fields.web` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fields.zipcode` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fieldsByName` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fieldsByName.billingAddress` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fieldsByName.deliveryAddress` | object |  |
| `extendedInfo.clientFolder.extendedInfo.fieldsByName.vATNumber` | object |  |
| `extendedInfo.clientFolder.extendedInfo.permalink` | string |  |
| `extendedInfo.clientFolder.extendedInfo.user` | object |  |
| `extendedInfo.clientFolder.extendedInfo.user.email` | string |  |
| `extendedInfo.clientFolder.extendedInfo.user.firstname` | string |  |
| `extendedInfo.clientFolder.extendedInfo.user.id` | number |  |
| `extendedInfo.clientFolder.extendedInfo.user.lastname` | string |  |
| `extendedInfo.clientFolder.extendedInfo.user.mobilePhone` | object |  |
| `extendedInfo.clientFolder.extendedInfo.user.phone` | object |  |
| `extendedInfo.clientFolder.id` | number |  |
| `extendedInfo.clientFolder.isActive` | boolean |  |
| `extendedInfo.clientFolder.name` | string |  |
| `extendedInfo.clientFolder.userId` | number |  |
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
| `probability` | number |  |
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

Through the native noCRM.io API, this operation is `POST /leads/:id/add_to_client` (base URL `{{credentials.baseUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-lead-to-client-folder.md) for the provider-specific parameters and requirements.

