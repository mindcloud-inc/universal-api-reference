# Recruitee ATS: List Candidates



```
GET https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/list-candidates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recruitee ATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/list-candidates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/list-candidates?${params}`, {
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
| `limit` | number | no | Specifies the number of candidates to retrieve. |
| `offset` | number | no | Skip number of candidates from the beginning. |
| `createdAfter` | string | no | Show only candidates created after the given date-time. |
| `disqualified` | boolean | no | Show only candidates disqualified in at least one job. |
| `qualified` | boolean | no | Show only candidates qualified in at least one job. |
| `ids` | string | no | Comma-separated list of candidate IDs. |
| `offerId` | number | no | Filter by offer. |
| `query` | string | no | Search query for candidate name or offer. |
| `sort` | string | no | Sorting option. Default: `by_date`. |
| `withMessages` | boolean | no | Show only candidates with messages. |
| `withMyMessages` | boolean | no | Show only candidates with messages sent by the current admin. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminappUrl": "https://example.com",
      "adminId": {},
      "createdAt": "string",
      "emails": [
        "ava@example.com"
      ],
      "example": true,
      "followed": true,
      "hasAvatar": true,
      "id": 1,
      "initials": "string",
      "isAnonymous": true,
      "isHired": true,
      "isRevealed": true,
      "lastMessageAt": {},
      "myLastRating": {},
      "myPendingResultRequest": true,
      "myUpcomingEvent": true,
      "name": "Ava Chen",
      "pendingResultRequest": true,
      "phones": [
        "string"
      ],
      "photoThumbUrl": "https://example.com",
      "placements": [
        {
          "candidateId": 1,
          "createdAt": "string",
          "departmentId": {},
          "departmentName": {},
          "hiredAt": {},
          "hiredById": {},
          "hiredInOtherPlacement": true,
          "hiredInThisPlacement": true,
          "id": 1,
          "jobStartsAt": {},
          "language": {},
          "offerId": {},
          "overdueAt": {},
          "overdueDiff": {},
          "position": 1,
          "positiveRatings": {},
          "ratingVisible": true,
          "stageId": {},
          "talentPoolId": 1,
          "updatedAt": "string"
        }
      ],
      "positiveRatings": {},
      "ratingsCount": 1,
      "ratingVisible": true,
      "referrer": {},
      "salutation": {},
      "source": "string",
      "tasksCount": 1,
      "title": {},
      "unreadNotifications": true,
      "upcomingEvent": true,
      "updatedAt": "string",
      "viewed": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminappUrl` | string |  |
| `adminId` | object |  |
| `createdAt` | string |  |
| `emails[]` | string |  |
| `example` | boolean |  |
| `followed` | boolean |  |
| `hasAvatar` | boolean |  |
| `id` | number |  |
| `initials` | string |  |
| `isAnonymous` | boolean |  |
| `isHired` | boolean |  |
| `isRevealed` | boolean |  |
| `lastMessageAt` | object |  |
| `myLastRating` | object |  |
| `myPendingResultRequest` | boolean |  |
| `myUpcomingEvent` | boolean |  |
| `name` | string |  |
| `pendingResultRequest` | boolean |  |
| `phones[]` | string |  |
| `photoThumbUrl` | string |  |
| `placements[].candidateId` | number |  |
| `placements[].createdAt` | string |  |
| `placements[].departmentId` | object |  |
| `placements[].departmentName` | object |  |
| `placements[].hiredAt` | object |  |
| `placements[].hiredById` | object |  |
| `placements[].hiredInOtherPlacement` | boolean |  |
| `placements[].hiredInThisPlacement` | boolean |  |
| `placements[].id` | number |  |
| `placements[].jobStartsAt` | object |  |
| `placements[].language` | object |  |
| `placements[].offerId` | object |  |
| `placements[].overdueAt` | object |  |
| `placements[].overdueDiff` | object |  |
| `placements[].position` | number |  |
| `placements[].positiveRatings` | object |  |
| `placements[].ratingVisible` | boolean |  |
| `placements[].stageId` | object |  |
| `placements[].talentPoolId` | number |  |
| `placements[].updatedAt` | string |  |
| `positiveRatings` | object |  |
| `ratingsCount` | number |  |
| `ratingVisible` | boolean |  |
| `referrer` | object |  |
| `salutation` | object |  |
| `source` | string |  |
| `tasksCount` | number |  |
| `title` | object |  |
| `unreadNotifications` | boolean |  |
| `upcomingEvent` | boolean |  |
| `updatedAt` | string |  |
| `viewed` | boolean |  |

## Native endpoint

Through the native Recruitee ATS API, this operation is `GET /c/:company_id/candidates` (base URL `https://api.recruitee.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-candidates.md) for the provider-specific parameters and requirements.

