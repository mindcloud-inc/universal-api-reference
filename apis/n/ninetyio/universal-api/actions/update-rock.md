# Ninety.io: Update Rock

Updates an existing rock in Ninety.io.

```
PUT https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/update-rock
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninety.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/update-rock" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/update-rock', {
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
| `userId` | string | no | The Id of the user who owns the Rock |
| `teamId` | string | no | The Id of the team the Rock belongs to |
| `title` | string | no | The title of the Rock |
| `description` | string | no | The description of the Rock |
| `statusCode` | string | no | The status of the Rock |
| `levelCode` | string | no | The level of the Rock |
| `quarter` | string | no | The quarter associated with the Rock |
| `dueDate` | date | no | The due date of the Rock |
| `rockQuarterYearDueDate` | date | no | The quarter-aligned year due date of the Rock |
| `archived` | boolean | no | Set to true to archive the Rock, false to unarchive it |
| `futureScope` | string | no | The future scope of the Rock |
| `additionalTeamIds[]` | array<string> | no | Array of additional team Ids that can also view this Rock |

## Response

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
      "createdByUserId": "string",
      "createdDate": "string",
      "deleted": true,
      "description": "string",
      "dueDate": "string",
      "dueDateQuarter": "string",
      "followers": [
        "string"
      ],
      "Id": "string",
      "levelCode": "string",
      "ordinal": 1,
      "planningBoardOrdinal": 1,
      "quarter": "string",
      "statusCode": "string",
      "teamId": "string",
      "title": "string",
      "updatedAt": "string",
      "updatedBy": "string",
      "userId": "string",
      "userOrdinal": 1,
      "V": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `archivedDate` | object |  |
| `companyId` | string |  |
| `completed` | boolean |  |
| `completedDate` | object |  |
| `createdByUserId` | string |  |
| `createdDate` | string |  |
| `deleted` | boolean |  |
| `description` | string |  |
| `dueDate` | string |  |
| `dueDateQuarter` | string |  |
| `followers[]` | string |  |
| `Id` | string |  |
| `levelCode` | string |  |
| `ordinal` | number |  |
| `planningBoardOrdinal` | number |  |
| `quarter` | string |  |
| `statusCode` | string |  |
| `teamId` | string |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `updatedBy` | string |  |
| `userId` | string |  |
| `userOrdinal` | number |  |
| `V` | number |  |

## Native endpoint

Through the native Ninety.io API, this operation is `PATCH /v1/rocks/:id` (base URL `https://api.public.ninety.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-rock.md) for the provider-specific parameters and requirements.

