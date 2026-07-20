# Ninety.io: Create Milestone

Creates a new milestone in Ninety.io.

```
POST https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/create-milestone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninety.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/create-milestone" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "rockId": "string",
  "title": "string",
  "dueDate": "2026-06-30T23:59:59.000Z",
  "teamId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/create-milestone', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "rockId": "string",
    "title": "string",
    "dueDate": "2026-06-30T23:59:59.000Z",
    "teamId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `rockId` | string | yes |  |
| `title` | string | yes |  |
| `dueDate` | date | yes | Example: `2026-06-30T23:59:59.000Z`. |
| `teamId` | string | yes |  |
| `description` | string | no | The description of the Milestone |
| `userOrdinal` | number | no | The ordinal position of this Milestone for the user |
| `toDoId` | string | no | The Id of a related To-Do item, if any |
| `isDone` | boolean | no | True if the Milestone is already done at creation time |
| `completedDate` | date | no | The date the Milestone was completed |

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
| `userOrdinal` | number |  |

## Native endpoint

Through the native Ninety.io API, this operation is `POST /v1/milestones` (base URL `https://api.public.ninety.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-milestone.md) for the provider-specific parameters and requirements.

