# noCRM.io: List Unassigned Leads

Retrieves unassigned leads from noCRM.io.

```
GET https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-unassigned-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a noCRM.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-unassigned-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/list-unassigned-leads?${params}`, {
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
      "amount": {},
      "attachmentCount": 1,
      "clientFolderId": {},
      "clientFolderName": {},
      "closedAt": {},
      "createdAt": "string",
      "createdById": {},
      "createdFrom": "string",
      "currency": {},
      "description": "string",
      "estimatedClosingDate": {},
      "htmlDescription": "string",
      "id": 1,
      "nextActionAt": "string",
      "pipeline": "string",
      "probability": {},
      "remindDate": {},
      "remindTime": {},
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
      "teamName": {},
      "title": "string",
      "updatedAt": "string",
      "userId": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | object |  |
| `attachmentCount` | number |  |
| `clientFolderId` | object |  |
| `clientFolderName` | object |  |
| `closedAt` | object |  |
| `createdAt` | string |  |
| `createdById` | object |  |
| `createdFrom` | string |  |
| `currency` | object |  |
| `description` | string |  |
| `estimatedClosingDate` | object |  |
| `htmlDescription` | string |  |
| `id` | number |  |
| `nextActionAt` | string |  |
| `pipeline` | string |  |
| `probability` | object |  |
| `remindDate` | object |  |
| `remindTime` | object |  |
| `starred` | boolean |  |
| `status` | string |  |
| `step` | string |  |
| `stepId` | number |  |
| `tags[]` | array<string> |  |
| `teamId` | object |  |
| `teamName` | object |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `userId` | object |  |

## Native endpoint

Through the native noCRM.io API, this operation is `GET /leads/unassigned` (base URL `{{credentials.baseUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-unassigned-leads.md) for the provider-specific parameters and requirements.

