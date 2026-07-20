# Ninety.io: Get Rock by Id

Retrieves a rock from Ninety.io by ID.

```
GET https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/get-rock-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninety.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/get-rock-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/get-rock-by-id?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |

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
      "originalDueDate": {},
      "planningBoardOrdinal": 1,
      "quarter": "string",
      "statusCode": "string",
      "teamId": "string",
      "title": "string",
      "updatedAt": {},
      "updatedBy": {},
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
| `originalDueDate` | object |  |
| `planningBoardOrdinal` | number |  |
| `quarter` | string |  |
| `statusCode` | string |  |
| `teamId` | string |  |
| `title` | string |  |
| `updatedAt` | object |  |
| `updatedBy` | object |  |
| `userId` | string |  |
| `userOrdinal` | number |  |
| `V` | number |  |

## Native endpoint

Through the native Ninety.io API, this operation is `GET /v1/rocks/:id` (base URL `https://api.public.ninety.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rock-by-id.md) for the provider-specific parameters and requirements.

