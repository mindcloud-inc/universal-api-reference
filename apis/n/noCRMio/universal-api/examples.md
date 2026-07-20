# noCRM.io Universal API Examples

These examples use the MindCloud API key and noCRM.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Leads

Retrieves leads from noCRM.io.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-leads?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-leads?${params}`, {
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
      "amount": 1,
      "clientFolderId": 1,
      "clientFolderName": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "pipeline": "string",
      "probability": 1,
      "starred": true,
      "status": "string",
      "step": "string",
      "stepId": 1,
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Leads action reference](actions/list-leads.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/noCRMio/latest/actions/list-leads).

## Add Lead To Client Folder

Adds a lead to a client folder in noCRM.io.

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

Example response:

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

See the full [Add Lead To Client Folder action reference](actions/add-lead-to-client-folder.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/noCRMio/latest/actions/add-lead-to-client-folder).
