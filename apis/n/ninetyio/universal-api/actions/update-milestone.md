# Ninety.io: Update Milestone

Updates an existing milestone in Ninety.io.

```
PUT https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/update-milestone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninety.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/update-milestone" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/update-milestone', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `title` | string | no | The title of the Milestone |
| `description` | string | no | The description of the Milestone |
| `dueDate` | date | no | The due date of the Milestone |
| `isDone` | boolean | no | Set to true to mark the Milestone as done |
| `ownedByUserId` | string | no | The Id of the user who owns this Milestone |
| `completedDate` | date | no | The date the Milestone was completed |
| `followers[]` | array<string> | no | Array of user Ids who are following this Milestone |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": "string",
      "createdBy": "string",
      "createdDate": "string",
      "description": {},
      "dueDate": "string",
      "followers": [
        "string"
      ],
      "Id": "string",
      "isDeleted": true,
      "isDone": true,
      "ownedByUserId": "string",
      "rockId": "string",
      "teamId": "string",
      "title": "string",
      "toDoId": {},
      "updatedAt": "string",
      "updatedBy": "string",
      "userOrdinal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | string |  |
| `createdBy` | string |  |
| `createdDate` | string |  |
| `description` | object |  |
| `dueDate` | string |  |
| `followers[]` | string |  |
| `Id` | string |  |
| `isDeleted` | boolean |  |
| `isDone` | boolean |  |
| `ownedByUserId` | string |  |
| `rockId` | string |  |
| `teamId` | string |  |
| `title` | string |  |
| `toDoId` | object |  |
| `updatedAt` | string |  |
| `updatedBy` | string |  |
| `userOrdinal` | number |  |

## Native endpoint

Through the native Ninety.io API, this operation is `PATCH /v1/milestones/:id` (base URL `https://api.public.ninety.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-milestone.md) for the provider-specific parameters and requirements.

