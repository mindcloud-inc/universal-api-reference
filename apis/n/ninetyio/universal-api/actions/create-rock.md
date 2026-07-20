# Ninety.io: Create Rock

Creates a new rock in Ninety.io.

```
POST https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/create-rock
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninety.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/create-rock" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "title": "Launch new customer onboarding flow",
  "dueDate": "2026-06-30T23:59:59.000Z",
  "statusCode": "CANCELED",
  "levelCode": "COMPANY",
  "quarter": "None"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/create-rock', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "title": "Launch new customer onboarding flow",
    "dueDate": "2026-06-30T23:59:59.000Z",
    "statusCode": "CANCELED",
    "levelCode": "COMPANY",
    "quarter": "None"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | list<string> | yes | The Id of the team the Rock belongs to |
| `title` | string | yes | The title of the Rock Example: `Launch new customer onboarding flow`. |
| `dueDate` | date | yes | The due date of the Rock (ISO 8601) Example: `2026-06-30T23:59:59.000Z`. |
| `statusCode` | list<string> | yes | The status of the Rock: OFF_TRACK, ON_TRACK, DONE, or CANCELED One of: `CANCELED`, `DONE`, `OFF_TRACK`, `ON_TRACK`. |
| `levelCode` | list<string> | yes | The level of the Rock: USER, COMPANY_AND_DEPARTMENT, COMPANY, or DEPARTMENT One of: `COMPANY`, `COMPANY_AND_DEPARTMENT`, `DEPARTMENT`, `USER`. |
| `quarter` | list<string> | yes | The quarter associated with the Rock: Q1, Q2, Q3, Q4, or None One of: `None`, `Q1`, `Q2`, `Q3`, `Q4`. |
| `description` | string | no | The description of the Rock Example: `Redesign the onboarding wizard to reduce drop-off by 20%`. |
| `additionalTeamIds[]` | list<string> | no | Additional team Ids that can also view this Rock Accepts multiple values as an array. |
| `futureScope` | list<string> | no | The future scope of the Rock: Current, Next, Later, or Future One of: `Current`, `Future`, `Later`, `Next`. |
| `rockQuarterYearDueDate` | date | no | The quarter-aligned year due date of the Rock (ISO 8601) Example: `2026-06-30T23:59:59.999Z`. |
| `addCreatorToFollowersList` | boolean | no | When true, the authenticated user is added to the Rock's followers list Default: `false`. |

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

Through the native Ninety.io API, this operation is `POST /v1/rocks` (base URL `https://api.public.ninety.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-rock.md) for the provider-specific parameters and requirements.

